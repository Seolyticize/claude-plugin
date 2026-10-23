---
name: rank-tracking-review
description: Review how a client's tracked keywords moved and why — positions, URL changes, SERP features, device split — and say what to do about it. Use for "how are rankings", "what dropped", "rank report".
---

# Rank tracking review

1. `list_rank_trackers` for the client, then `get_rank_summary` for the headline movement.
2. `get_position_distribution` over 30 or 90 days — is the shape improving (more in 1–3 and 4–10) or not?
3. Drill into movers with `get_rank_history` (filter by device if the tracker reads both; desktop and mobile are separate series).
4. For every significant drop, check `get_url_swaps`: a different page ranking is cannibalisation or a canonical problem, not a content problem. Confirm with `get_cannibalization`.
5. `get_serp_features` — a drop in clicks with a steady position often means a feature (AI overview, video, local pack) arrived above the result.
6. Pinned keywords (`list_tracked_keywords`) lead the review; they are the ones the team agreed matter.
7. Be exact about absence: a keyword "not in the results" was read and missing; one with no capture was not read. Never treat either as position 0 or 100.
8. Recommend concrete actions per keyword group, then add a `research` entry to the brief. If the person wants it for the client, write it up with `save_written_report`.
