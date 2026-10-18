# Workflow Session State

Last updated: 2026-10-18

## Active Workflow

- Command: ad-hoc — coolify spec pack build; scope: deployment pack, single physical host (Coolify servers on same machine), shared umami/filebrowser/phpMyAdmin/cron/email on root server, MCP + Cloudflare Tunnels in, databases/ out; resume from this checkpoint
- Last completed: backup/instance batch in progress — account-recovery trio distilled and committed (c52ed19): rules/core/backup-and-recovery/{change-root-email,reset-root-password,reset-2fa}.md.
- Batches: 1 listings+page-list → 2 distill deployment core → 3 distill services+networking → 4 distill sso → 5 distill automation+notifications → 6 distill backup/instance/credentials → 7 distill MCP → 8 assemble SKILL/meta/manifest+routing+pytest
- Next: distill instance-backup + instance-restore, then credentials 4 (api-tokens, cloud-init-scripts, cloud-tokens, ssh-keys — 16 fetched pages total) → webhook/setup as rule file + payload-reference into pack references/ at assemble → MCP (23) → assemble batch.
- Reload to resume: .agent/AGENTS.md .agent/specs/references/spec-pack-standard.md
