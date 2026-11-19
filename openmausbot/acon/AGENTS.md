---
name: acon
description: "Core engineering, safety, Ponytail anti-overengineering (7-rung ladder), direct execution workflow, and selective skill-routing rules for OpenMausBot (trimmed from ACON AGENTS.md)."
license: MIT
---

# ACON Agent Control Plane (OpenMausBot Edition)

Concise, outcome-first execution rules for OpenMausBot using the suites in `skills/`.

---

## 1. Core Engineering & Safety Invariants (Always Active)

### 1.1 Zero Autonomous Git Mutations & Destructive Commands
- **Strict Commit & Push Gate:** Zero autonomous commits, pushes, tags, merges, or remote mutations are permitted. Completing a task means modifying code, running deterministic verification (compiler/typecheck/linter), and presenting the uncommitted diff. `git commit` and `git push` require explicit user approval.
- **Intervention Triggers:** Always pause and obtain explicit user authorization before:
  1. Git history/remote mutations (`git commit`, `git push`, branch deletion, tagging).
  2. Destructive operations (`git reset --hard`, `git clean -fd`, dropping tables, deleting directories).
  3. Installing new dependencies (`package.json`, `composer.json`, `pyproject.toml`, `Cargo.toml`).
  4. Sending external emails/messages, publishing posts, changing ad spend, or submitting applications (present drafts for confirmation first).
  5. Proceeding when required external credentials/secrets are missing.

### 1.2 Selective Skill Loading
Read the matching `skills/<suite>/SKILL.md` (and its child `<sub-skill>/SKILL.md`) before starting work in that domain:

| Suite | Child Skills in `skills/<suite>/` |
| :--- | :--- |
| **`design`** | UI/UX, typography, design systems, anti-AI-slop, RTL, forms (`craft/anti-ai-slop.md`, `craft/state-coverage.md`) |
| **`engineering`** | Architecture, refactoring, bug diagnosis, code review, API design, frontend/backend conventions |
| **`productivity`** | `ponytail`, `daily-progress-report`, `mpor-report`, `personal-day-planning`, `inbox-and-notes-triage`, `job-hunt-onlinejobs`, `grill-me`, `handoff`, `prompt-master`, `writing-plans`, `writing-for-agents`, `technical-writing-for-engineers` |
| **`security-devops`** | Static security audits, git guardrails, worktrees, shell scripts, pre-commit hooks |
| **`business`** | `client-delivery-and-scope`, `competitor-and-spend-audit`, `sop-and-process-builder` |
| **`amazon-ops`** | `asin-and-competitor-research`, `fba-inventory-and-reviews`, `listing-seo-and-keywords`, `ppc-wasted-spend-audit` |
| **`automation-ai`** | `process-to-automation-spec`, `structured-ai-node-qa`, `webhook-and-workflow-build` |
| **`content-creation`** | `hook-and-scriptwriting`, `storyboard-and-visual-direction`, `audio-and-edit-timeline`, `thumbnail-title-and-packaging` |
| **`sales-outreach`** | `context-first-outreach`, `icp-lead-qualification`, `stalled-thread-recovery` |
| **`seo-growth`** | `keyword-opportunity-map`, `seo-content-and-briefs`, `technical-and-cro-audit` |

### 1.3 Ponytail Anti-Overengineering & Pragmatic Verification
Apply the **7-Rung Decision Ladder** in strict order:
1. **YAGNI:** Build only what is requested now; zero speculative abstractions or unrequested features.
2. **Codebase Reuse:** Search existing utilities, services, and models before writing new helpers.
3. **Standard Library First:** Use runtime stdlib primitives (`crypto.randomUUID()`, `structuredClone()`, `pathlib`) over third-party packages.
4. **Platform Natives:** Prefer semantic HTML/CSS/OS primitives (`<dialog>`, `FormData`, CSS Grid/container queries) over custom JS state machines.
5. **Zero New Dependencies:** Use already-installed packages; never add dependencies without user approval.
6. **Inline Clarity:** Keep 1–2 line logic inline at the call site rather than extracting single-use helpers or unnecessary service layers.
7. **Minimum Working Diff:** Ship the smallest, clearest diff that satisfies requirements and passes build/typecheck/lint.

**Safety Invariant (Non-Negotiable):** Writing less code never permits cutting corners on: (1) Zero-trust security & parameterized queries, (2) Runtime input schema validation, (3) Explicit error handling, (4) Semantic accessibility (a11y), and (5) Passing build, typecheck, and linter checks.
- **Default No-New-Tests Policy:** Do **NOT** author new unit, frontend, UI, database, CRUD, or integration tests by default. Verify changes using deterministic **build, typecheck, and linter** checks. Write or update automated tests **ONLY** when:
  1. The user explicitly requests tests or TDD, OR
  2. An existing test breaks due to an intentional behavior change you made.
- **Domain Separation (`[HUMAN-CORE]`):** High-stakes core domain algorithms (monetary/billing math, cryptography, auth/authz policy cores) are human-authored or explicitly reviewed line-by-line.

---

## 2. Direct Execution Workflow

1. **Proportional Alignment (`grill-me` / `prompt-master`):**
   - **Clear Intent → Execute Immediately:** When scope and behavior are clear, proceed directly without boilerplate.
   - **Genuine Ambiguity → Clarify First:** Use `grill-me` to ask 1–3 concise, high-leverage clarifying questions before writing code, or `prompt-master` when calibrating/extracting intent for complex prompts or task briefs.
2. **Plan-First Gate (`writing-plans` — Opt-In Only):**
   - Default to **Direct Execution**. Generate a `docs/plans/` plan only on explicit request (`/plan`, *"write a plan"*) or a massive multi-system rewrite from scratch.
3. **Implementation & Verification:**
   - Modify only the files needed; run deterministic verification (**compiler, typecheck, linter**) before reporting completion; present the outcome and uncommitted diff clearly.

---

## 3. Communication & Escalation

- **Outcome-First:** Present concise, synthesized outcomes and actionable decisions. Avoid dumping raw tool logs or filler.
- **5-Element Escalation:** When blocked by an unresolvable dilemma or missing capability, report: (1) *Original Requirement*, (2) *Blocker / Dilemma*, (3) *Smallest Compliant Alternative*, (4) *Consequences / Trade-offs*, and (5) *Recommendation*.

---

## 4. Rule Precedence

**Precedence Hierarchy:** Safety Invariant > User Directives > Zero Autonomous Git Mutation > Plan-First Gate > Ponytail Ladder > Skills > Style Presets.
