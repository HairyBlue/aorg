---
name: fba-inventory-and-reviews
description: Prevent stockouts, flag stranded SKUs, and turn customer return/review patterns into product or copy fixes.
license: MIT
metadata:
  title: FBA Restock Math & Review Root-Cause Triage
  version: "1"
  author: AORG
  tags: amazon-ops, workflow
---

Use this when the user needs to prevent stockouts, flag stranded SKUs, and turn customer return/review patterns into product or copy fixes.

1. Confirm the requested scope and available evidence, then follow the workflow below. Reuse answers already supplied.

# FBA Restock Math & Review Root-Cause Triage

## Process
1. Compute Days of Cover = (Available + Inbound FBA units) / weighted daily velocity, and compare against supplier + shipping + FBA check-in lead time.
2. Group negative reviews and returns by root cause (defect, sizing, misleading copy/photo, shipping damage) and propose concrete listing or supplier fixes.

Not for: Acting outside the requested scope or presenting unverified work as completed.
Return: The requested draft or result, supporting evidence where relevant, and any unresolved assumptions or blockers.
Approval: Ask before sending, publishing, purchasing, booking, cancelling, deleting, changing live systems, installing dependencies, committing or pushing, or enabling recurring automation. Drafts and reviews alone do not authorize those actions.
