---
name: ai-visibility-audit
description: Check whether AI assistants (ChatGPT, Claude, Perplexity, Gemini, Google AI Overviews and others) recommend a client, which rivals they name instead, which sources they rely on, and what would change it. Use for "AI visibility", "are we in ChatGPT", "GEO", "LLM SEO".
---

# AI visibility audit

1. `get_ai_visibility_setup`: questions, brands (exactly one marked as the client), schedule, and which assistants this agency can ask. If nothing is set up, use `suggest_ai_prompts` and save the agreed questions with `save_ai_visibility_setup` (needs `client:manage`).
2. Before any paid run, `estimate_ai_visibility_cost` — then `run_ai_visibility_check` with `maxCostMicros` once the person agrees. Results arrive in minutes; poll `get_ai_visibility_runs`.
3. `get_ai_visibility_results` for the latest run: which questions the client is missing from, and who is named instead. Read a few full answers with `get_ai_visibility_answer` — the wording explains a lot.
4. `get_ai_visibility` for share of voice and the sources assistants cite; `get_ai_visibility_trend` for direction over time.
5. `get_agent_readiness` — whether assistants' crawlers can read the site at all.
6. To check a single question before tracking it, `explore_ai_prompt` asks it live (nothing stored).
7. Recommend: pages to create or strengthen for the questions missed, publications to get onto (the cited sources), and crawler or rendering fixes. A question with an answer the client is absent from is a finding; an answer that was never captured is not.
8. Record a `research` entry; save a written report if asked.
