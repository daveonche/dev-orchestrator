# Workflow Session State

Last updated: 2026-10-18

## Active Workflow

- Command: ad-hoc — coolify spec pack build; scope: deployment pack, single physical host (Coolify servers on same machine), shared umami/filebrowser/phpMyAdmin/cron/email on root server, MCP + Cloudflare Tunnels in, databases/ out; resume from this checkpoint
- Last completed: 8a-2 index applied (trusted contents) but commit REJECTED by commit-msg hook (subject 123 > 72) — corrected command provided; 8a-3 drafted (30 entries → 111 total).
- Batches: 1 listings+page-list → 2 distill deployment core → 3 distill services+networking → 4 distill sso → 5 distill automation+notifications → 6 distill backup/instance/credentials → 7 distill MCP → 8 assemble SKILL/meta/manifest+routing+pytest
- Next: commit with short subject → 8b SKILL.meta.md → 8c manifest + upgrade-notes + payload-reference git mv → 8d routing row (/add .agent/AGENTS.md) + pytest tests/test_s4_2_step1.py.
- Reload to resume: .agent/AGENTS.md .agent/specs/references/spec-pack-standard.md
