---
name: acon-core
description: "Core execution, safety, YAGNI, and selective skill-routing rules for OpenMausBot workspaces (trimmed from ACON AGENTS.md without session/orchestrator harness)."
license: MIT
---

# ACON Core (OpenMausBot Edition)

Concise, outcome-first execution rules for OpenMausBot.

## 1. Core Safety & Approval Gates

- **Zero Autonomous Git & Destructive Actions:** Never run `git commit`, `git push`, branch deletion, tagging, `git reset --hard`, `git clean -fd`, or delete data/directories without explicit user approval.
- **Zero Autonomous External Sends:** Never send external emails/messages, publish posts, change ad spend, or submit applications automatically—present drafts for confirmation first.
- **Zero Unrequested Dependencies:** Do not install new packages without explicit user approval.

## 2. Selective Skill Routing

Before starting domain work, check and follow the matching skill in `skills/`:

- **Business Ops:** `client-delivery-and-scope`, `competitor-and-spend-audit`, `sop-and-process-builder`
- **Amazon Ops:** `asin-and-competitor-research`, `fba-inventory-and-reviews`, `listing-seo-and-keywords`, `ppc-wasted-spend-audit`
- **Automation & AI:** `process-to-automation-spec`, `structured-ai-node-qa`, `webhook-and-workflow-build`
- **Content Creation:** `hook-and-scriptwriting`, `storyboard-and-visual-direction`, `audio-and-edit-timeline`, `thumbnail-title-and-packaging`
- **Sales Outreach:** `context-first-outreach`, `icp-lead-qualification`, `stalled-thread-recovery`
- **SEO & Growth:** `keyword-opportunity-map`, `seo-content-and-briefs`, `technical-and-cro-audit`
- **Design:** `design` (UI/UX, visual hierarchy, aesthetic presets)
- **Engineering:** `engineering` (architecture, refactoring, bug diagnosis, code review)
- **Productivity:** `productivity` (`ponytail`, `daily-progress-report`, `mpor-report`, `personal-day-planning`, `inbox-and-notes-triage`, `job-hunt-onlinejobs`, `grill-me`, `handoff`, `prompt-master`)
- **Security & DevOps:** `security-devops` (security audits, git safety/worktrees, shell scripts, pre-commit)

## 3. Pragmatic Execution (YAGNI)

1. **Clear Intent → Execute Immediately:** Ask 1–3 brief clarifying questions only when genuine ambiguity exists.
2. **Reuse & Simplicity:** Reuse existing files, templates, and standard tools; avoid speculative abstractions.
3. **Verification:** Verify changes with deterministic build, typecheck, or lint checks; do not write unrequested test suites unless asked.
4. **Outcome-First Communication:** Lead with the result, decision, or draft—no filler.
