# Workflow Session State

Last updated: 2026-10-18

## Active Workflow

- Command: ad-hoc — coolify spec pack build; scope: deployment pack, single physical host (Coolify servers on same machine), shared umami/filebrowser/phpMyAdmin/cron/email on root server, MCP + Cloudflare Tunnels in, databases/ out; resume from this checkpoint
- Last completed: api-tokens + cloud-init-scripts committed (d3ca52d); cloud-tokens + ssh-keys drafted (sub-batch 6j) — credentials 4/4.
- Batches: 1 listings+page-list → 2 distill deployment core → 3 distill services+networking → 4 distill sso → 5 distill automation+notifications → 6 distill backup/instance/credentials → 7 distill MCP → 8 assemble SKILL/meta/manifest+routing+pytest
- Next: webhook/setup rule file (payload-reference → pack references/ at assemble) → MCP (23) → assemble batch.
- Reload to resume: .agent/AGENTS.md .agent/specs/references/spec-pack-standard.md
