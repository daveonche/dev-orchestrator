# Core › Notifications › Channels › Webhook › Setup

Source: coollabsio/coolify-docs `content/docs/core/notifications/channels/webhook/setup.mdx` @ main `3b7c416`.

## Endpoint prerequisites

- Accepts `POST` over HTTP/HTTPS with a JSON body; reachable from the Coolify instance; records requests for verification; returns a successful response PROMPTLY (no long-running work); handles duplicate deliveries (retries happen).
- Initial test: development endpoint or request inspector showing method, headers, body; move to production after the test succeeds.

## Configure

1. **Notifications > Webhook** → enter the endpoint in **Webhook URL** → **Save changes**.
2. **Enable** — a valid webhook URL is required first.
3. **Notification events**: select the events to send.
4. **Send test** → verify at the endpoint: method `POST`, valid JSON body, `"event": "test"`, prompt successful response.

- A received test proves reachability + request format, NOT that every event-specific field is handled by your application.

## Endpoint requirements

- URL scheme `http` or `https` with a valid host.
- Rejected for server-side request protection: `localhost`, `0.0.0.0`, IPv6 loopback, `127.0.0.0/8`, link-local `169.254.0.0/16` (cloud metadata endpoints), hostnames ending in `.internal`.
- Private-network IPs are accepted, but the Coolify instance still needs a network route to the endpoint.

## Delivery behavior

- Deliveries are queued and sent with Laravel's HTTP client; up to 5 total attempts with a 10-second backoff after an unhandled exception.
- A non-2xx response does NOT fail the job — return 2xx when the event is accepted and use receiver-side logs/monitoring to detect rejected requests.
- No signature or shared-secret header: use an unguessable HTTPS URL or an authenticated gateway when the endpoint is internet-exposed.

## Troubleshoot a failed test

1. URL starts with `http(s)://` + complete path → 2. not in a blocked loopback/link-local/`.internal` range → 3. from the Coolify server's network: DNS resolves + firewall allows → 4. receiver access/application logs (a request can reach a reverse proxy but fail before the app records it) → 5. endpoint accepts `POST` + JSON and responds promptly → 6. private IP: the instance has a route to that network.

- Test succeeds but a production event does not arrive: confirm the event is enabled under **Notification events** and compare the receiver's parser with the payload reference.
