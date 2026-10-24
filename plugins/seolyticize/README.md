# Seolyticize for Claude Code

The Claude Code plugin manifest for Seolyticize's agent skills. The skills themselves are the canonical set in [`skills/`](../../skills) at the repository root; `scripts/public-repos.mjs claude-plugin` copies them in when it publishes [Seolyticize/claude-plugin](https://github.com/Seolyticize/claude-plugin).

## Install

```
/plugin marketplace add Seolyticize/skills
/plugin install seolyticize@seolyticize
```

[Seolyticize/skills](https://github.com/Seolyticize/skills) is the main home of the skills, with install paths for every other agent host too. `Seolyticize/claude-plugin` keeps working for anyone who added it before, with the same skills.

## Skills

Eighteen workflows: `seolyticize` (the foundation: ways in, conventions, and which skill to load for what), client onboarding, the weekly loop, technical audits and fixing them in code, release checks, keyword research, content opportunities, briefs and writing, rank reviews, competitors, link building, local SEO, AI visibility, analytics and conversions, monthly reports, spend and costs, and alerts and monitoring.

## How every skill behaves

- It reads the client brief first and records what it concluded in the brief's research log.
- It quotes before it spends, tells you the cost, and passes the quote as `maxCostMicros` so a call cannot cost more than agreed.
- Bulk writes are previewed with `dryRun` first.
- It never turns unknown into zero, and says when a figure is partial or a heuristic.
