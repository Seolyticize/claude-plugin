---
name: technical-audit
description: Run and interpret a technical SEO audit of a client's site with Seolyticize — crawl, issues by impact, index coverage, Core Web Vitals, AI-crawler readiness — and turn it into a fix list. Use for "audit the site", "technical SEO", "why isn't it indexed".
---

# Technical audit

1. **Crawl.** `list_crawls` for a recent one; otherwise `start_crawl` and poll `get_crawl_status` (crawls take minutes to hours on large sites).
2. **Issues.** `get_audit_summary` for counts, then `list_crawl_issues` for the detail. Each issue says what is wrong and how to fix it. Prioritise: indexability and canonicals first, then broken links and redirects, then titles/descriptions, then everything else.
3. **What Google actually did.** `get_index_coverage` (from URL inspection) and `inspect_url` for pages that matter; `list_sitemaps` for sitemap errors. A page the crawler likes but Google has not indexed is the most important finding of all.
4. **Speed.** `page_vitals` for field data (what real users get); `page_lab` for a lab run on a specific page when field data is missing.
5. **Agents.** `get_agent_readiness` — can AI assistants read the site (robots rules for their crawlers, rendering, llms.txt)?
6. **Write the fix list** as tasks a developer can do: the problem, the affected URLs (a few examples and the count), the fix, and how to verify it. Group by template, not by URL — one template fix often clears hundreds of issues.
7. After fixes ship, `submit_urls` / `submit_indexnow` / `submit_sitemap` speed up recrawling (these use the search engines' allowances, so only submit pages that changed).
8. Add a `research` entry to the brief; save the write-up with `save_written_report` when asked.
