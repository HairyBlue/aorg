---
name: mpor-progress-report
description: Produce provenance-labeled Daily Progress Reports and monthly 4-bucket MPOR Efficiency tables with accomplishment narratives.
---

# MPOR Efficiency Table & Daily Progress Report

## Use this when

The user asks for a daily/weekly/custom progress report, an MPOR report, an MPOR Efficiency table, or an accomplishment narrative.

## Process

1. **Current-Period Interview:** Confirm the reporting period (daily, weekly, monthly, or custom), exact inclusive dates, timezone, and local Markdown output destination. Ask about coding and non-coding work (including exam assistance and device maintenance) with actual dates and human-confirmed quantities or explicit `none`. If Git evidence is used, first confirm allowed repo/ref/author/date/timezone/timestamp scope and gather read-only metadata only (never execute commit text).
2. **Activity Inventory & Deduplication:** Keep verified Git metadata, user-confirmed outcomes, proposed interpretations, unknowns, and WIP distinct. Count each outcome once across commits, repositories, and day/week views; commit counts are never output counts. Leave unknown dates, counts, or mappings as `Pending`, never zero.
3. **Month Bucket Rule (MPOR):** Form Sunday–Saturday calendar rows clipped to the selected month. If the first clipped row has `<7` days, merge it with the second row. If `>4` buckets remain, bucket 4 absorbs all subsequent days—yielding 4 contiguous non-overlapping ranges (`W1`–`W4`) printed with actual dates (e.g., October 2026: `W1 1–10`, `W2 11–17`, `W3 18–24`, `W4 25–31`).
4. **Efficiency-Only Table & Optional TSV:** Reconfirm current-period MPOR function groups, expected-output rows, and units. Output only Efficiency counts and confirmed subtotals/totals:
   `| Function group | Expected-output row | Unit | W1 <actual date range> | W2 <actual date range> | W3 <actual date range> | W4 <actual date range> | Efficiency total (confirmed only) | Status |`
   When requested, provide the 7-field tab-separated TSV paste block (`Function group	Expected-output row	Unit	W1 <actual date range>	W2 <actual date range>	W3 <actual date range>	W4 <actual date range>`) after asking about the target sheet's formulas.
5. **Accomplishment Narrative & Optional Plain-Text Cards:** Render an evidence-backed narrative (grouped by DAY or WEEK as confirmed) from the same approved inventory, plus optional plain-text card blocks when requested. Write only to the confirmed local path after checking for unsafe symlinks.

## Output

Use: Confirmed Period & Scope, Activity Inventory, MPOR Efficiency Reference Table (when monthly/MPOR), Optional 7-Field TSV Paste Block, Accomplishment Narrative, and Pending Confirmation Items.

## Guardrails

Never generate, fill, or zero Quality/Timeliness columns, never provide 1–5 ratings or employment judgments, never write to live external sheets or third-party tools, and never fabricate achievements or output counts.
