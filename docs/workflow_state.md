# Workflow Session State

Last updated: 2026-10-17

## Active Workflow

- Command: ad-hoc — coolify spec pack build; scope: deployment pack, single physical host (Coolify servers on same machine), shared umami/filebrowser/phpMyAdmin/cron/email on root server, MCP + Cloudflare Tunnels in, databases/ out; resume from this checkpoint
- Last completed: Batch 2 complete — configuration distilled: 6 rules files under .agent/specs/coolify/rules/applications/configuration/ (general, environment-variables, health-checks, persistent-storage, resource-limits, advanced); configuration/overview skimmed and folded into SKILL.md per no-overview-rule-files convention.
- Batches: 1 listings+page-list → 2 distill deployment core → 3 distill services+networking → 4 distill ops+mcp → 5 assemble SKILL/meta/manifest+routing+pytest
- Next: Batch 3 — /read-only the 6 pending third-level listings (proxy/caddy, proxy/traefik, cloudflare/tunnels, channels/webhook, authentication/oauth, authentication/sso — already fetched) to enumerate their pages; then fetch + distill services/configuration and core/networking groups.
- Reload to resume: .agent/AGENTS.md .agent/specs/references/spec-pack-standard.md
