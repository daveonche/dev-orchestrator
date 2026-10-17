# Applications › Builds › Dockerfile

Source: coollabsio/coolify-docs `content/docs/applications/builds/dockerfile.mdx` @ main `3b7c416`.

## Where the Dockerfile lives
- Two paths: **Git repository** (build context = **Base Directory**; **Dockerfile Location** relative to it) or **Dockerfile without Git** (stored under **General > Dockerfile**).
- Without Git there is no build context: `COPY`/`ADD` cannot read repository files.
- Creation label is **Build pack**; after creation it is **Build strategy** under **General > Build pipeline**.

## Runtime wiring
- Set **Ports Exposes** to the internal listening port; the process must bind `0.0.0.0`, not `127.0.0.1`, or the proxy cannot reach it.
- Without-Git apps: the first `EXPOSE` becomes the initial **Ports Exposes**; initial port is `80` when there is no `EXPOSE`.
- Runtime settings (domains, env vars, storage, health checks, limits) are not baked into the image.
- Never copy production secrets into the Dockerfile or image layers.

## Build arguments and secrets
- **Advanced > Build > Build arguments** → **Managed manually in Dockerfile** when the Dockerfile declares and consumes every `ARG` itself.
- `SOURCE_COMMIT` is excluded from Git-based builds by default (cache reuse across commits); set **Source commit availability** → **Available during build** only when the image contents need it.
- Sensitive build-time values: **Build secrets > Docker BuildKit secrets** (requires BuildKit).

## Health checks
- Image-level `HEALTHCHECK` works; the image must contain the check command. Alternatively configure under **Healthcheck** (see `rules/applications/configuration/health-checks.md` for precedence).

## Deployment commands
- **Pre-deployment** runs in the current container before replacement; skipped when no current container exists (first deployment); failure stops the deployment.
- **Post-deployment** runs in the new container; deployment is marked complete before it runs; failure is logged but does not change the successful status.
- Both must be safe to run repeatedly; test migrations against non-production.

## Build succeeds, domain fails
1. **Runtime Logs** for exit/bind errors → 2. confirm `0.0.0.0` binding → 3. confirm **Ports Exposes** → 4. health-check request inside **Terminal** → 5. no-available-server guide.
