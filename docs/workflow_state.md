# Workflow Session State

Last updated: 2026-10-17

## Active Workflow

- Command: ad-hoc — coolify spec pack build; scope: deployment pack, single physical host (Coolify servers on same machine), shared umami/filebrowser/phpMyAdmin/cron/email on root server, MCP + Cloudflare Tunnels in, databases/ out; resume from this checkpoint
- Last completed: Batch 3 traefik group 1 distilled: 5 rules files under .agent/specs/coolify/rules/core/networking/proxy/traefik/ (basic-auth, custom-middlewares, custom-ssl-certs, dashboard, dns-challenge); traefik overview skimmed and folded into SKILL.md per no-overview-rule-files convention.
- Batches: 1 listings+page-list → 2 distill deployment core → 3 distill services+networking → 4 distill ops+mcp → 5 assemble SKILL/meta/manifest+routing+pytest
- Next: /read-only traefik group 2 (.log/coolify-docs-core-networking-proxy-traefik-{dynamic-config,load-balancing,protect-services-with-authentik,tls-certificates,update,wildcard-certs}-page.mdx, already fetched) and distill; then tunnels/webhook/oauth/sso and automation/notifications groups (all already fetched).
- Reload to resume: .agent/AGENTS.md .agent/specs/references/spec-pack-standard.md
