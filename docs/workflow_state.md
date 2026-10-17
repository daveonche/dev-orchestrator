# Workflow Session State

Last updated: 2026-10-17

## Active Workflow

- Command: ad-hoc — coolify spec pack build; scope: deployment pack, single physical host (Coolify servers on same machine), shared umami/filebrowser/phpMyAdmin/cron/email on root server, MCP + Cloudflare Tunnels in, databases/ out; resume from this checkpoint
- Last completed: Batch 2a group 1 distilled: 6 rules files created under .agent/specs/coolify/rules/applications/builds/ (dockerfile, docker-compose, docker-registries, custom-docker-options, static, railpack); builds/overview skimmed and folded into SKILL.md per no-overview-rule-files convention.
- Batches: 1 listings+page-list → 2 distill deployment core → 3 distill services+networking → 4 distill ops+mcp → 5 assemble SKILL/meta/manifest+routing+pytest
- Next: fetch 2b pages — for p in applications/sources/overview applications/sources/public-repositories applications/sources/deploy-keys applications/sources/gitlab applications/sources/bitbucket applications/sources/gitea applications/sources/other-providers applications/sources/cursor-origin applications/sources/github/overview applications/sources/github/actions applications/sources/github/app applications/sources/github/auto-deploy applications/sources/github/deploy-key applications/sources/github/preview-deploy applications/sources/github/public-repository applications/sources/github/switch-apps applications/configuration/overview applications/configuration/general applications/configuration/environment-variables applications/configuration/health-checks applications/configuration/persistent-storage applications/configuration/resource-limits applications/configuration/advanced; do curl -fsSL "https://raw.githubusercontent.com/coollabsio/coolify-docs/main/content/docs/$p.mdx" > ".log/coolify-docs-$(echo $p | tr '/' '-')-page.mdx"; done — then /read-only the 8 sources pages and distill.
- Reload to resume: .agent/AGENTS.md .agent/specs/references/spec-pack-standard.md
