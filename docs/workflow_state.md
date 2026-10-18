# Workflow Session State

Last updated: 2026-10-18

## Active Workflow

- Command: ad-hoc — coolify spec pack build; scope: deployment pack, single physical host (Coolify servers on same machine), shared umami/filebrowser/phpMyAdmin/cron/email on root server, MCP + Cloudflare Tunnels in, databases/ out; resume from this checkpoint
- Last completed: backup/instance batch in progress — 5 rules/core/backup-and-recovery/ files committed: account-recovery trio (c52ed19) + instance-backup/instance-restore (1729ad7).
- Batches: 1 listings+page-list → 2 distill deployment core → 3 distill services+networking → 4 distill sso → 5 distill automation+notifications → 6 distill backup/instance/credentials → 7 distill MCP → 8 assemble SKILL/meta/manifest+routing+pytest
- Next: distill instance-management 7 (downgrade, update, instance-settings, reverb-migration, uninstallation, environment-variables, update-coolify-database) → credentials 4 → webhook/setup rule file (payload-reference → pack references/ at assemble) → MCP (23) → assemble batch.
- Reload to resume: .agent/AGENTS.md .agent/specs/references/spec-pack-standard.md
