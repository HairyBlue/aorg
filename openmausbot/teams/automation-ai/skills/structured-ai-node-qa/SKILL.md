---
name: structured-ai-node-qa
description: Lock down AI workflow steps with strict JSON schemas and untrusted-input guardrails.
---

# Structured LLM Node & Prompt Hardening

## Process
1. Define the system prompt, strict JSON output schema (including `confidence` and `needs_human_review`), 3 realistic test payloads (normal, missing fields, adversarial/noisy input), and the fallback branch when confidence is low.
