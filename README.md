# Seolyticize for Claude Code

SEO workflows — onboarding a site, technical audits, rank tracking reviews, content opportunities, AI visibility, monthly reports — as Claude Code skills over the [Seolyticize](https://seolyticize.com) MCP server.

## Install

```
/plugin marketplace add Seolyticize/claude-plugin
/plugin install seolyticize@seolyticize
```

The plugin connects to `https://seolyticize.com/api/mcp`; Claude Code signs you in the first time. Prefer a key? `claude mcp add --transport http seolyticize https://seolyticize.com/api/mcp --header "Authorization: Bearer $SEOLYTICIZE_API_KEY"`.

## Other agents

Any MCP client can connect to `https://seolyticize.com/api/mcp`:

- **Claude (web/desktop), ChatGPT, Cursor:** add it as a custom connector / remote MCP server; they sign in the same way.
- **Clients without OAuth:** create an API key under Settings → API keys and send it as `Authorization: Bearer <key>`.

## Workflows

| Skill                 | For                                                                        |
| --------------------- | -------------------------------------------------------------------------- |
| client-onboarding     | Create a client, draft its brief from the site, connect and start tracking |
| keyword-research      | Expand seeds, judge difficulty and intent, shortlist and save              |
| rank-tracking-review  | Explain movements: URL swaps, SERP features, device split                  |
| technical-audit       | Crawl, index coverage, vitals, agent readiness, a fix list                 |
| content-opportunities | Near-misses valued by GA4, decay, cannibalisation, gaps                    |
| competitor-analysis   | Search competitors, gaps, link intersect, AI mentions                      |
| link-prospecting      | Realistic link prospects and pitch angles                                  |
| ai-visibility-audit   | What assistants say, who they name, what they cite                         |
| monthly-client-report | The client-facing report, saved and shareable                              |

Every workflow reads the client brief first, quotes paid calls with `estimate_cost` before making them (and passes the quote as `maxCostMicros`), and records its conclusions in the brief's research log.

License: MIT.
