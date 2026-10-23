---
name: client-onboarding
description: Set up a new SEO client in Seolyticize — create the client, write its brief from its website, connect what can be connected, and start tracking. Use when someone says "onboard", "add a new client", or "set up <business>".
---

# Onboard a client

Work through these in order. Stop and ask when a step needs a decision only the person can make (budget, which competitors matter, what to track).

1. **Who am I?** Call `whoami`. Onboarding needs `client:manage` for creating clients and saving AI-visibility setup; if the role lacks it, say what is missing and stop.
2. **Create the client** with `create_client` (name, monthly budget if given), then `create_project` with the site's domain and market. Use `list_markets` to find the location code; never guess one.
3. **Write the brief.** Call `draft_client_brief` — quote it first with `estimate_cost` (`{"tool":"draft_client_brief","arguments":{"clientId":…}}`) and pass the figure as `maxCostMicros`. Show the draft. Save only what the person confirms with `update_client_brief`; leave anything marked "Not stated on the site." for them to fill. Ask for the current goal and the main competitors — the site will not say.
4. **Connections.** `get_client_integrations` shows what is connected. Search Console, GA4 and Bing need the site owner's consent through the Manage page — give the person the link to that page rather than trying to connect them yourself.
5. **Tracking.** `create_rank_tracker`, then `add_tracked_keywords` with the terms agreed. Before adding, quote a month with `estimate_cost` on `add_tracked_keywords`. Pin the handful that matter most with `pin_tracked_keywords`.
6. **AI visibility** (optional). `suggest_ai_prompts`, then `save_ai_visibility_setup` with the chosen questions and the brands (exactly one `isClient`). Show `estimate_ai_visibility_cost` before `set_ai_visibility_schedule`.
7. **First crawl.** `start_crawl`; check back with `get_crawl_status`.
8. **Record it.** Add a `research` entry to the brief with `update_client_brief` summarising what was set up and what is still waiting on the client.
