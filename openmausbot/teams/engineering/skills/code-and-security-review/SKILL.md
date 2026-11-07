---
name: code-and-security-review
description: Audit uncommitted diffs for simplicity, runtime safety, OWASP vulnerabilities, and git guardrails.
---

# Independent Code Quality & Security Audit

## Use this when

Reviewing an uncommitted implementation diff before Tech Lead presents the final work to the user, or when auditing a repository for bugs and security risks.

## Process

1. **Maintain Reviewer Independence:** Run as a read-only auditor (`qa-reviewer` / `devops-guard`). Never audit code authored in the same worker turn.
2. **Code Quality Audit:** Check simplicity, absence of dead code or single-use wrapper bloat, UI modular file size (`<=300` lines), explicit error handling, and deterministic `build`/`typecheck`/`lint` pass evidence. Do not flag missing unit/UI tests unless the user explicitly requested tests.
3. **Security Audit:** Inspect all modified trust boundaries for SQL/command/template injection, broken object-level authorization (IDOR), missing runtime schema validation, SSRF, XSS, hardcoded secrets/tokens, and unsafe path/symlink traversal.
4. **Git & Release Guardrails:** Confirm no autonomous `git commit`, `git push`, or unapproved dependency changes occurred.

## Output

Use: Verdict (`Ready`, `Ready with minor notes`, or `Blocked`), Findings by Severity (`Critical`, `High`, `Medium`, `Low`) with `file:line` references, and Minimal Remediation Diffs.

## Guardrails

Never invent hypothetical vulnerabilities without a concrete code path, and never mutate files during a read-only review pass.
