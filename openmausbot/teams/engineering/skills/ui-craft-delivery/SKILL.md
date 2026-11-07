---
name: ui-craft-delivery
description: Build crafted, accessible interfaces with full state coverage and modular files under 300 lines.
---

# Clean UI Craft & Modular Frontend

## Use this when

Designing, building, refactoring, or auditing frontend pages, dashboards, modals, forms, or design systems.

## Process

1. **Reuse Existing Primitives:** Inspect existing UI components (`components/ui/`, buttons, modals, inputs, toasts) and design tokens before writing markup. Never reinvent shared primitives inside feature files.
2. **Eliminate Generic Slop:** Establish crisp typographic hierarchy, intentional surface elevation, and cohesive spacing/color tokens that match the repository's aesthetic direction.
3. **Complete State Coverage:** Explicitly implement loading, empty, error, success, keyboard focus/navigation, and responsive small-screen states for every interactive view.
4. **Enforce Modular File Limits:** Keep every component and page file `<=300` lines by extracting cohesive sub-components, custom hooks, or type definitions into focused sibling files.

## Output

Use: Reused Primitives, Component File Line Counts (`<=300` lines), Covered Interactive States, and Build/Typecheck/Rendered Verification.

## Guardrails

Do not introduce unapproved UI libraries or icon packs. Do not write unrequested frontend snapshot or unit test files unless explicitly asked by the user.
