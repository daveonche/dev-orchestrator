# Workflow Session State

Last updated: 2026-10-17

## Active Workflow

- Command: ad-hoc — coolify spec pack build; scope: deployment pack, single physical host (Coolify servers on same machine), shared umami/filebrowser/phpMyAdmin/cron/email on root server, MCP + Cloudflare Tunnels in, databases/ out; resume from this checkpoint
- Last completed: Batch 3 services/configuration distilled: 5 rules files under .agent/specs/coolify/rules/services/configuration/ (general, docker-compose, environment-variables, networking, persistent-storage); services overview skimmed and folded into SKILL.md per no-overview-rule-files convention.
- Batches: 1 listings+page-list → 2 distill deployment core → 3 distill services+networking → 4 distill ops+mcp → 5 assemble SKILL/meta/manifest+routing+pytest
- Next: /read-only the 4 caddy pages (.log/coolify-docs-core-networking-proxy-caddy-{overview,basic-auth,custom-ssl-certs,dns-challenge}-page.mdx, already fetched) and distill; then traefik (12 pages, already fetched) in two groups.
- Reload to resume: .agent/AGENTS.md .agent/specs/references/spec-pack-standard.md
