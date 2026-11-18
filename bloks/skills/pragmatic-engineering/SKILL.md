---
name: pragmatic-engineering
description: Ship the smallest, safest working diff verified by deterministic build, typecheck, and lint checks.
license: MIT
metadata:
  title: Pragmatic Anti-Overengineering & Direct Verification
  version: "1"
  author: AORG
  tags: engineering, workflow
---

Use this when the user needs to ship the smallest, safest working diff verified by deterministic build, typecheck, and lint checks.

1. Confirm the requested scope and available evidence, then follow the workflow below. Reuse answers already supplied.

# Pragmatic Anti-Overengineering & Direct Verification

## Process
1. **YAGNI:** Build only what is requested now; zero speculative abstractions or unrequested features.
2. **Codebase Reuse:** Search existing utilities, services, and models before creating new helpers.
3. **Standard Library & Platform Natives First:** Prefer runtime stdlib primitives (`crypto.randomUUID()`, `structuredClone()`, `pathlib`) and semantic HTML/CSS primitives (`<dialog>`, `FormData`, CSS Grid) over third-party libraries.
4. **Zero Unapproved Dependencies:** Use already-installed packages; never add dependencies without explicit approval.
5. **Minimum Working Diff:** Keep 1-2 line logic inline and touch only the files required.
6. **Pragmatic Verification:** Verify via deterministic compiler, typecheck, and linter checks. Do not write new unit, UI, or database test suites unless explicitly requested or an existing test breaks due to an intentional behavior change.

Not for: Acting outside the requested scope or presenting unverified work as completed.
Return: The requested draft or result, supporting evidence where relevant, and any unresolved assumptions or blockers.
Approval: Ask before sending, publishing, purchasing, booking, cancelling, deleting, changing live systems, installing dependencies, committing or pushing, or enabling recurring automation. Drafts and reviews alone do not authorize those actions.
