# Workflow Session State

Last updated: 2026-10-18

## Active Workflow

- Command: ad-hoc — coolify spec pack build; scope: deployment pack, single physical host (Coolify servers on same machine), shared umami/filebrowser/phpMyAdmin/cron/email on root server, MCP + Cloudflare Tunnels in, databases/ out; resume from this checkpoint
- Last completed: 8a-1 skeleton committed (50088f4); extraction run (112 files); 8a-2 index drafted: applications (26) + core (55 entries, payload-reference excluded → References index) — bulk normalize + rename still uncommitted in worktree.
- Batches: 1 listings+page-list → 2 distill deployment core → 3 distill services+networking → 4 distill sso → 5 distill automation+notifications → 6 distill backup/instance/credentials → 7 distill MCP → 8 assemble SKILL/meta/manifest+routing+pytest
- Next: commit normalize+rename+8a-2 → 8a-3 index integrations+mcp+services (30) → 8b SKILL.meta.md → 8c manifest + upgrade-notes + payload-reference git mv → 8d routing row (/add .agent/AGENTS.md) + pytest tests/test_s4_2_step1.py.
- Reload to resume: .agent/AGENTS.md .agent/specs/references/spec-pack-standard.md
