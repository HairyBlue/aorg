---
name: webhook-and-workflow-build
description: Build resilient automation flows with deduplication, retries, and clean error alerts.
---

# Idempotent n8n / Make / Webhook Design

## Process
1. Provide the exact node-by-node sequence, payload mappings, credential store references (never raw keys), idempotency check so re-runs never create duplicate records, and dead-letter error alert step.
