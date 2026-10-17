# Workflow Session State

Last updated: 2026-10-17

## Active Workflow

- Command: ad-hoc — coolify spec pack build; resume from this checkpoint
- Last completed: Docs source pinned: coollabsio/coolify-docs content/docs main@3b7c416; 6 section listings in .log/; scope: deployment pack, single physical host (Coolify servers on same machine), shared umami/filebrowser/phpMyAdmin/cron/email on root server, MCP + Cloudflare Tunnels in, databases/ proposed out.
- Batches: 1 listings+page-list → 2 distill deployment core → 3 distill services+networking → 4 distill ops+mcp → 5 assemble SKILL/meta/manifest+routing+pytest
- Next: Batch 1 — run: for p in applications/builds applications/configuration applications/deployments applications/sources core/automation core/notifications core/networking core/infrastructure core/persistent-storage core/backup-and-recovery core/security core/instance-management integrations/networking services/configuration; do curl -fsSL "https://api.github.com/repos/coollabsio/coolify-docs/contents/content/docs/$p?ref=main" > ".log/coolify-docs-$(echo $p | tr '/' '-')-listing-main.json"; done — then add all 14 listings and finalize the page list.
- Reload to resume: .agent/AGENTS.md .agent/specs/references/spec-pack-standard.md
