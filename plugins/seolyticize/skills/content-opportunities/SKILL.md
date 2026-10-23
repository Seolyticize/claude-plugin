---
name: content-opportunities
description: Find the content work worth doing first for a client — pages near the top three, pages losing traffic, pages competing with each other, and topics competitors cover that the client does not. Use for "content plan", "what should we write or update", "quick wins".
---

# Content opportunities

1. `get_client_brief` for the goal and voice, then `get_opportunities` for the overview in one call — each part says if it could not be read.
2. **Update before you write.** `get_search_opportunities` ranks pages around positions 4–20 by what their organic visitors are worth in GA4; without GA4, `striking_distance` ranks them by extra clicks. These are the cheapest wins.
3. **Stop the bleeding.** `get_content_decay` lists pages losing clicks; check each with `get_url_swaps` and `get_serp_features` before blaming the content.
4. **Rewrite snippets.** `get_low_ctr_queries` — page-one queries clicking far below their position. Check `get_serp_features` first; otherwise rewrite the title and description to answer the query.
5. **Untangle.** `get_cannibalization` — two pages splitting one query; recommend which to keep, merge or re-target.
6. **New topics.** `get_content_gap` and `get_keyword_gap` against the competitors in the brief; validate demand with `keyword_explorer` (quote first).
7. **Measure what matters.** `get_ga4_landing_pages` and `get_ga4_key_events` show which pages convert; a traffic gain on a page that converts beats a bigger gain on one that does not.
8. Output a prioritised plan: update / consolidate / create, each with the target query, the page, the expected gain and the reasoning. Mark figures that are estimates as estimates.
9. Record the plan as a `research` entry; save it as a report if asked.
