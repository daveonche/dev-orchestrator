# Workflow Session State

Last updated: 2026-10-17

## Active Workflow

- Command: ad-hoc — coolify spec pack build; scope: deployment pack, single physical host (Coolify servers on same machine), shared umami/filebrowser/phpMyAdmin/cron/email on root server, MCP + Cloudflare Tunnels in, databases/ out; resume from this checkpoint
- Last completed: Batch 3 tunnels+webhook distilled: 6 rules files under .agent/specs/coolify/rules/ (integrations/networking/cloudflare/tunnels/: all-resource, single-resource, server-ssh, full-tls; core/notifications/channels/webhook/: setup, payload-reference); tunnels index skimmed and folded into SKILL.md.
- Batches: 1 listings+page-list → 2 distill deployment core → 3 distill services+networking → 4 distill ops+mcp → 5 assemble SKILL/meta/manifest+routing+pytest
- Next: /read-only oauth (8 fetched pages: .log/coolify-docs-core-security-authentication-oauth-*-page.mdx) and distill; then sso (5) → automation/notifications (16) → backup/instance/credentials (18) → MCP (23) — all fetched; Batch 5 assembles SKILL/meta/manifest+routing+pytest.
- Reload to resume: .agent/AGENTS.md .agent/specs/references/spec-pack-standard.md
