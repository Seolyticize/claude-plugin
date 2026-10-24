# Seolyticize for Claude Code

SEO workflows — onboarding a site, technical audits, rank tracking reviews, content opportunities, AI visibility, monthly reports — as Claude Code skills over the [Seolyticize](https://seolyticize.com) MCP server.

## Install

```
/plugin marketplace add Seolyticize/claude-plugin
/plugin install seolyticize@seolyticize
```

The same skills, with install paths for Codex, Cursor, Copilot, Gemini and every other agent, are in [Seolyticize/skills](https://github.com/Seolyticize/skills).

The plugin connects to `https://seolyticize.com/api/mcp`; Claude Code signs you in the first time. Prefer a key? `claude mcp add --transport http seolyticize https://seolyticize.com/api/mcp --header "Authorization: Bearer $SEOLYTICIZE_API_KEY"`.

## Skills

Eighteen workflows: `seolyticize` (the foundation: ways in, conventions, and which skill to load for what), client onboarding, the weekly loop, technical audits and fixing them in code, release checks, keyword research, content opportunities, briefs and writing, rank reviews, competitors, link building, local SEO, AI visibility, analytics and conversions, monthly reports, spend and costs, and alerts and monitoring.

## How every skill behaves

- It reads the client brief first and records what it concluded in the brief's research log.
- It quotes before it spends, tells you the cost, and passes the quote as `maxCostMicros` so a call cannot cost more than agreed.
- Bulk writes are previewed with `dryRun` first.
- It never turns unknown into zero, and says when a figure is partial or a heuristic.

License: MIT.
