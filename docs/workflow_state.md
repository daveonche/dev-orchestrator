# Workflow Session State

Last updated: 2026-10-18

## Active Workflow

- Command: ad-hoc — coolify spec pack build; scope: deployment pack, single physical host (Coolify servers on same machine), shared umami/filebrowser/phpMyAdmin/cron/email on root server, MCP + Cloudflare Tunnels in, databases/ out; resume from this checkpoint
- Last completed: checkpoint saved (0d45254); style decision: normalize to GFM blank-line-after-heading, 7f first (4 files to edit, 2 already compliant); 8a format refs in context (docker SKILL.md/SKILL.meta.md, elgg source-listing-7.1.1.json).
- Batches: 1 listings+page-list → 2 distill deployment core → 3 distill services+networking → 4 distill sso → 5 distill automation+notifications → 6 distill backup/instance/credentials → 7 distill MCP → 8 assemble SKILL/meta/manifest+routing+pytest
- Next: /add 4 dropped 7f files (logs, integrations, prompts-and-resources, pagination) → normalize heading blank lines → decide: extend normalize to remaining ~106 rules or keep compact → 8a SKILL.md (fold 5 overviews; 112-file index incl. build-from-dockerfile.md) → 8b SKILL.meta.md → 8c manifest + upgrade-notes + payload-reference git mv → 8d routing row (/add .agent/AGENTS.md) + pytest tests/test_s4_2_step1.py.
- Reload to resume: .agent/AGENTS.md .agent/specs/references/spec-pack-standard.md
