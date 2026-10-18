# Workflow Session State

Last updated: 2026-10-18

## Active Workflow

- Command: ad-hoc — coolify spec pack build; scope: deployment pack, single physical host (Coolify servers on same machine), shared umami/filebrowser/phpMyAdmin/cron/email on root server, MCP + Cloudflare Tunnels in, databases/ out; resume from this checkpoint
- Last completed: 8b committed (0042a83; tree clean confirms); manifest reconciled: content/docs @ main listing is the provenance artifact — the v4.4.6-tagged listing covers repo docs/, not content/docs; 8c drafted (git mv payload-reference, cp manifest, upgrade-notes .gitkeep, SKILL.md index fix).
- Batches: 1 listings+page-list → 2 distill deployment core → 3 distill services+networking → 4 distill sso → 5 distill automation+notifications → 6 distill backup/instance/credentials → 7 distill MCP → 8 assemble SKILL/meta/manifest+routing+pytest
- Next: apply 8c (mv+cp+gitkeep+index fix) and commit → 8d routing row (/add .agent/AGENTS.md) + pytest tests/test_s4_2_step1.py + optional v4.4.6 tag verification.
- Reload to resume: .agent/AGENTS.md .agent/specs/references/spec-pack-standard.md
