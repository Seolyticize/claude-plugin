---
name: keyword-research
description: Find and shortlist keywords for a client with Seolyticize — expand seeds, filter by volume and difficulty, check intent and the live results page, and save the shortlist. Use for "keyword research", "find keywords", "what should we target".
---

# Keyword research

1. **Context.** `get_client_brief` — the overview, audience and goal decide which keywords are worth anything. If the brief is empty, ask the person for the business and audience before spending money.
2. **Market.** `list_markets` for the location code. Keep one market per piece of research.
3. **Expand seeds.** For each seed, quote `keyword_explorer` with `estimate_cost`, tell the person the total, then call it with `maxCostMicros`. Modes: `ideas` (broad), `related`, `suggestions` (longer phrasings), `questions` (what people actually ask). Filtering, sorting and paging an expansion already bought is free — refine with the explorer's filters rather than buying again.
4. **Judge difficulty properly.** For candidates you would recommend, `explain_keyword_difficulty` says why a keyword is hard (who ranks, how strong they are). `serp_overview` shows the page itself; `keyword_traffic_potential` says what the top result really earns across all its keywords — use it to pick the parent topic rather than chasing variants.
5. **Already ranking?** `striking_distance` and `get_search_opportunities` show terms the client nearly ranks for — usually the cheapest wins. Put them first.
6. **Shortlist.** Group by topic and intent. For each, give volume, difficulty, the page that should rank (existing or new), and why. Unknown figures are unknown — say "not reported", never 0.
7. **Save.** `create_keyword_list` / `add_keywords_to_list` for the shortlist; `add_tracked_keywords` only for the ones the person wants tracked (quote the month first).
8. **Record.** Add a `research` entry to the brief with the conclusions and the list name.
