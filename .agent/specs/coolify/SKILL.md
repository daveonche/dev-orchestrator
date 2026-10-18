# Coolify Conventions

Delta conventions for administering the self-hosted Coolify instance that
deploys this repository's projects: applications, services, networking,
notifications, security, instance management, MCP, and Cloudflare Tunnel
integrations. This pack records only repo-relevant rules and
easily-got-wrong details; general Coolify knowledge (dashboard navigation,
deployment concepts, provider basics) is assumed. Consult the Coolify
documentation when needed. Database resources are out of scope: the
upstream `databases/` section was not distilled.

**Source:** Coolify documentation — coollabsio/coolify-docs `content/docs`
@ main `3b7c416` (v4.4.6 snapshot), upstream docs at
[coolify.io/docs](https://coolify.io/docs).

**Scope:** Coolify administration tasks in this repository — instance
management, applications, services, networking (DNS, domains, proxy),
notifications, security (authentication, credentials), MCP, and
Cloudflare Tunnel integrations. Deployment context: single physical host,
Coolify servers on the same machine, shared umami/filebrowser/phpMyAdmin/
cron/email on the root server, MCP and Cloudflare Tunnels in scope,
`databases/` out.

**Convention Check Reminder:** Before creating or editing any file, check the Conventions Reference Routing table in `.agent/AGENTS.md` and load the matching reference via `/read-only` before proceeding.

## Role

You are a Coolify conventions reviewer for this repository. Priorities,
in order:

1. Operational safety: destructive actions (uninstall, restore, downgrade,
   password/2FA resets, key rotation) carry explicit warnings in the rules;
   never soften or skip them.
2. Least privilege and secret hygiene: tokens, keys, and webhook URLs are
   secrets — scope them to one team, prefer `read`/`deploy` over `root`,
   store them in secret managers, revoke on exposure.
3. Version accuracy: rules apply to the version recorded in the provenance
   manifest; run the freshness check before relying on any rule.
4. Delta-only guidance: do not add general Coolify practices, API
   references, or tutorials to this pack.

## Before advising

1. Locate the task's area: instance management, applications, services,
   networking, notifications, security, MCP, or integrations. Detection is
   read-only; it never modifies project files.
2. Freshness check: before using any `rules/` topic, compare the version
   in `references/source-listing-4.4.6.json` against the latest stable
   Coolify release; if a newer stable exists, prompt to fetch that
   release's source listing and refresh the affected
   `references/upgrade-notes/` and `rules/` files before relying on them.
3. Load the task-matched rule files from the index below before giving
   guidance.

## Rules index

<!-- rules index: 112 entries appended in 8a-2/8a-3; payload-reference moves to references/ in 8c -->

## References index

- `references/source-listing-4.4.6.json` — upstream source manifest for
  the distilled version; freshness-check input.
- `references/upgrade-notes/` — version-specific upgrade notes (empty at
  the v4.4.6 baseline).
- `references/webhook-payload-reference.md` — per-event webhook JSON
  payload reference (moved from `rules/` in 8c).

## Language pack

None — Coolify is a technology pack, not a framework pack.

## Gotchas

- Tags are team-scoped and stored lowercase; they group resources for
  navigation and bulk deploy but change no configuration, and deploy
  webhooks act only within the token's team.
- A notification requires both an enabled channel and selected events;
  **Send test** verifies credential delivery, not every selected event.
- Scheduled tasks, database backups, volume backups, and Docker cleanups
  each have their own per-minute scheduler; a busy type does not delay the
  others. Schedules run in the owning server's configured timezone, and
  fixed-time schedules run once when DST repeats an hour.
- Instance backups cover Coolify's database only — never application,
  database, or volume data — and `APP_KEY` must be saved separately or the
  backup cannot be restored.
- MCP returns only the token team's resources; environment values are
  never returned, and log redaction is best effort.
- `@every_minute` is not a supported named schedule — use `every_minute`.
- All MCP list tools return paginated data — read the pagination rule
  before iterating through large results.
- Editor tooling associates `Dockerfile*` filenames with Dockerfile
  syntax; the Dockerfile build rule is therefore named
  `build-from-dockerfile.md`.

## How to use

- Load only the rule files matching the task at hand; never load the pack
  "just in case".
- After editing anything in this pack, run
  `python3 -m pytest tests/test_s4_2_step1.py`.

<!-- sentinel: specs/coolify -->
