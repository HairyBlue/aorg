---
name: team-orchestration
description: Coordinate alignment, file-boundary mapping, parallel implementation, and verification.
license: MIT
metadata:
  title: Engineering Orchestration & Synthesis
  version: "1"
  author: AORG
  tags: engineering, workflow
---

Use this when the user needs to coordinate alignment, file-boundary mapping, parallel implementation, and verification.

1. Confirm the requested scope and available evidence, then follow the workflow below. Reuse answers already supplied.

# Engineering Orchestration & Synthesis

## Process
1. **Alignment:** Execute clear requests immediately; ask 1-3 concise clarifying questions only when genuine architectural forks exist; write a formal plan only when explicitly requested.
2. **Recon:** Delegate read-only reconnaissance to `scout` and `researcher` to identify existing reusable utilities and partition the work into strictly non-overlapping file sets.
3. **Parallel Build:** Dispatch `backend`, `frontend`, and `fullstack` concurrently across disjoint file scopes. Once implementation and deterministic checks (`build`, `typecheck`, `lint`) pass, run `qa-reviewer` for an independent read-only code and security audit.
4. **Synthesis:** Present the uncommitted diff and verification evidence to the user. Never run `git commit`, `git push`, destructive commands, or dependency installations without explicit authorization.

Bloks room boundary: Engineering and Engineering Review are separate teams. Request an independent review from the review room when available. If it is not installed or cannot be reached, tell the user; never pretend it ran or substitute a writer as their own independent reviewer.

Not for: Acting outside the requested scope or presenting unverified work as completed.
Return: The requested draft or result, supporting evidence where relevant, and any unresolved assumptions or blockers.
Approval: Ask before sending, publishing, purchasing, booking, cancelling, deleting, changing live systems, installing dependencies, committing or pushing, or enabling recurring automation. Drafts and reviews alone do not authorize those actions.
