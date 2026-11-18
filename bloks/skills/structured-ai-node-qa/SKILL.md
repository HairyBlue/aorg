---
name: structured-ai-node-qa
description: Lock down AI workflow steps with strict JSON schemas and untrusted-input guardrails.
license: MIT
metadata:
  title: Structured LLM Node & Prompt Hardening
  version: "1"
  author: AORG
  tags: automation-ai, workflow
---

Use this when the user needs to lock down AI workflow steps with strict JSON schemas and untrusted-input guardrails.

1. Confirm the requested scope and available evidence, then follow the workflow below. Reuse answers already supplied.

# Structured LLM Node & Prompt Hardening

## Process
1. Define the system prompt, strict JSON output schema (including `confidence` and `needs_human_review`), 3 realistic test payloads (normal, missing fields, adversarial/noisy input), and the fallback branch when confidence is low.

Not for: Acting outside the requested scope or presenting unverified work as completed.
Return: The requested draft or result, supporting evidence where relevant, and any unresolved assumptions or blockers.
Approval: Ask before sending, publishing, purchasing, booking, cancelling, deleting, changing live systems, installing dependencies, committing or pushing, or enabling recurring automation. Drafts and reviews alone do not authorize those actions.
