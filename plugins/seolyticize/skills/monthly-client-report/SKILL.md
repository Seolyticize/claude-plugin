---
name: monthly-client-report
description: Write the monthly SEO report a client actually reads — what changed, why, what it earned, and what happens next — using the agency's report template, saved to Seolyticize and shareable by link. Use for "monthly report", "client update", "write up results".
---

# Monthly client report

1. `get_client_brief` (audience, voice, goal) and `list_report_templates` for the client. If a template fits, follow its sections, tone and sign-off exactly.
2. Gather, for the last full month against the one before:
   - `get_ga4_overview` (organic sessions, key events, revenue) and `get_ga4_landing_pages`;
   - `get_search_console_performance` (clicks, impressions, position);
   - `get_rank_summary` and `get_position_distribution`;
   - `get_ai_visibility_trend` if AI visibility is tracked;
   - the research log in the brief for the work done.
3. Write for the client, not for an SEO: lead with outcomes (enquiries, revenue, visibility), explain movements in plain words, credit the work that caused them, and be straight about what did not move. Every number from a tool; say "not measured" where a figure is missing — never round it to zero.
4. End with next month's plan, tied to the goal in the brief.
5. Save with `save_written_report` (Markdown; tables are fine), naming the template. If the person wants a link for the client, `set_report_sharing` — only when asked.
6. Add a `research` entry noting the report and its headline.
