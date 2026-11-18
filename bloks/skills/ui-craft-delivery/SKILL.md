---
name: ui-craft-delivery
description: Build crafted, accessible interfaces with full state coverage and modular files under 300 lines.
license: MIT
metadata:
  title: Clean UI Craft & Modular Frontend
  version: "1"
  author: AORG
  tags: engineering, workflow
---

Use this when the user needs to build crafted, accessible interfaces with full state coverage and modular files under 300 lines.

1. Confirm the requested scope and available evidence, then follow the workflow below. Reuse answers already supplied.

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

Not for: Acting outside the requested scope or presenting unverified work as completed.
Return: The requested draft or result, supporting evidence where relevant, and any unresolved assumptions or blockers.
Approval: Ask before sending, publishing, purchasing, booking, cancelling, deleting, changing live systems, installing dependencies, committing or pushing, or enabling recurring automation. Drafts and reviews alone do not authorize those actions.
