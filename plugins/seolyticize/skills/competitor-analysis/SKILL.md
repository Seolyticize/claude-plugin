---
name: competitor-analysis
description: Work out who a client really competes with in search and where they are winning — search competitors, share of voice, keyword and content gaps, link gaps, and AI-assistant mentions. Use for "competitor analysis", "who are we up against", "why is X beating us".
---

# Competitor analysis

1. Start from the brief's competitors (`get_client_brief`) — business rivals — then find **search** competitors with `find_serp_competitors` on the client's tracked or shortlisted keywords (quote first; exclude the client's own domain). They are often different sites.
2. `get_share_of_voice` for the tracked set; `get_domain_facts` for each serious competitor's age, popularity and footprint.
3. `get_keyword_gap` and `get_content_gap`: what they rank for that the client does not, grouped by topic and intent.
4. `get_link_intersect`: sites linking to two or more competitors but not the client — the best link prospects.
5. `get_ai_visibility` and `get_ai_visibility_results`: which competitors assistants name instead of the client, and on which questions.
6. Summarise per competitor: where they win, why (content, links, features, brand), and the two or three moves that would close the gap. Update the brief's competitor entries with `update_client_brief` if the person agrees.
