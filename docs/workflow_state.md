# Workflow Session State

Last updated: 2026-10-17

## Active Workflow

- Command: ad-hoc — coolify spec pack build; scope: deployment pack, single physical host (Coolify servers on same machine), shared umami/filebrowser/phpMyAdmin/cron/email on root server, MCP + Cloudflare Tunnels in, databases/ out; resume from this checkpoint
- Last completed: Batch 3 traefik complete — group 2 distilled: 6 rules files under .agent/specs/coolify/rules/core/networking/proxy/traefik/ (dynamic-config, load-balancing, protect-services-with-authentik, tls-certificates, update, wildcard-certs); traefik section fully distilled (11 rules files).
- Batches: 1 listings+page-list → 2 distill deployment core → 3 distill services+networking → 4 distill ops+mcp → 5 assemble SKILL/meta/manifest+routing+pytest
- Next: /read-only tunnels+webhook (7 pages, already fetched: .log/coolify-docs-integrations-networking-cloudflare-tunnels-{index,all-resource,single-resource,server-ssh,full-tls}-page.mdx + .log/coolify-docs-core-notifications-channels-webhook-{setup,payload-reference}-page.mdx) and distill; then oauth/sso → automation/notifications → backup/instance/credentials (all fetched); MCP pages are the only unfetched group.
- Reload to resume: .agent/AGENTS.md .agent/specs/references/spec-pack-standard.md
