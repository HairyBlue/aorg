---
name: webhook-and-workflow-build
description: Build resilient automation flows with deduplication, retries, and clean error alerts.
license: MIT
metadata:
  title: Idempotent n8n / Make / Webhook Design
  version: "1"
  author: AORG
  tags: automation-ai, workflow
---

Use this when the user needs to build resilient automation flows with deduplication, retries, and clean error alerts.

1. Confirm the requested scope and available evidence, then follow the workflow below. Reuse answers already supplied.

# Idempotent n8n / Make / Webhook Design

## Process
1. Provide the exact node-by-node sequence, payload mappings, credential store references (never raw keys), idempotency check so re-runs never create duplicate records, and dead-letter error alert step.

Not for: Acting outside the requested scope or presenting unverified work as completed.
Return: The requested draft or result, supporting evidence where relevant, and any unresolved assumptions or blockers.
Approval: Ask before sending, publishing, purchasing, booking, cancelling, deleting, changing live systems, installing dependencies, committing or pushing, or enabling recurring automation. Drafts and reviews alone do not authorize those actions.
