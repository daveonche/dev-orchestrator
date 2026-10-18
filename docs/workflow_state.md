# Workflow Session State

Last updated: 2026-10-18

## Active Workflow

- Command: ad-hoc — coolify spec pack build; scope: deployment pack, single physical host (Coolify servers on same machine), shared umami/filebrowser/phpMyAdmin/cron/email on root server, MCP + Cloudflare Tunnels in, databases/ out; resume from this checkpoint
- Last completed: references-index fix committed (849db76); 8c file ops failed — references/ dir missing (cp ran before mkdir, command-order bug); tree clean, nothing applied; corrected chain provided.
- Batches: 1 listings+page-list → 2 distill deployment core → 3 distill services+networking → 4 distill sso → 5 distill automation+notifications → 6 distill backup/instance/credentials → 7 distill MCP → 8 assemble SKILL/meta/manifest+routing+pytest
- Next: run corrected 8c chain (mkdir → git mv → cp+gitkeep) → commit → pytest tests/test_s4_2_step1.py (log to .log/) → 8d routing row (AFM.md ref first) → optional v4.4.6 tag check.
- Reload to resume: .agent/AGENTS.md .agent/specs/references/spec-pack-standard.md
