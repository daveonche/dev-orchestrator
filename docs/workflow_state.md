# Workflow Session State

Last updated: 2026-10-18

## Active Workflow

- Command: ad-hoc — coolify spec pack build; scope: deployment pack, single physical host (Coolify servers on same machine), shared umami/filebrowser/phpMyAdmin/cron/email on root server, MCP + Cloudflare Tunnels in, databases/ out; resume from this checkpoint
- Last completed: webhook/setup committed (fb446bf) — notifications complete; stray duplicate distillation found in setup.md, dedup fix drafted (keep pack-style version).
- Batches: 1 listings+page-list → 2 distill deployment core → 3 distill services+networking → 4 distill sso → 5 distill automation+notifications → 6 distill backup/instance/credentials → 7 distill MCP → 8 assemble SKILL/meta/manifest+routing+pytest
- Next: distill MCP 21 rule files (mcp-overview + capabilities-overview fold into SKILL.md at assemble) in sub-batches 7a–7e → assemble batch (SKILL/meta/manifest+routing+pytest; payload-reference → pack references/).
- Reload to resume: .agent/AGENTS.md .agent/specs/references/spec-pack-standard.md
