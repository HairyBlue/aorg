---
name: pragmatic-engineering
description: Ship the smallest, safest working diff verified by deterministic build, typecheck, and lint checks.
---

# Pragmatic Anti-Overengineering & Direct Verification

## Process
1. **YAGNI:** Build only what is requested now; zero speculative abstractions or unrequested features.
2. **Codebase Reuse:** Search existing utilities, services, and models before creating new helpers.
3. **Standard Library & Platform Natives First:** Prefer runtime stdlib primitives (`crypto.randomUUID()`, `structuredClone()`, `pathlib`) and semantic HTML/CSS primitives (`<dialog>`, `FormData`, CSS Grid) over third-party libraries.
4. **Zero Unapproved Dependencies:** Use already-installed packages; never add dependencies without explicit approval.
5. **Minimum Working Diff:** Keep 1–2 line logic inline and touch only the files required.
6. **Pragmatic Verification:** Verify via deterministic compiler, typecheck, and linter checks. Do not write new unit, UI, or database test suites unless explicitly requested or an existing test breaks due to an intentional behavior change.
