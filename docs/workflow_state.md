# Workflow Session State

Last updated: 2026-10-18

## Active Workflow

- Command: ad-hoc — coolify spec pack build; scope: deployment pack, single physical host (Coolify servers on same machine), shared umami/filebrowser/phpMyAdmin/cron/email on root server, MCP + Cloudflare Tunnels in, databases/ out; resume from this checkpoint
- Last completed: 8c applied+committed (b49565f: manifest, upgrade-notes .gitkeep, payload-reference rename 100%); pytest tests/test_s4_2_step1.py OK; 8d routing row drafted (AFM.md criteria applied).
- Batches: 1 listings+page-list → 2 distill deployment core → 3 distill services+networking → 4 distill sso → 5 distill automation+notifications → 6 distill backup/instance/credentials → 7 distill MCP → 8 assemble SKILL/meta/manifest+routing+pytest
- Next: apply 8d routing row → commit → v4.4.6 tag check (ls-remote; fix SKILL.md Source line + manifest name if mismatch) → workflow complete: clear Active Workflow section.
- Reload to resume: .agent/AGENTS.md
