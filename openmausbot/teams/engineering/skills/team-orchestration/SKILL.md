---
name: team-orchestration
description: Coordinate alignment, file-boundary mapping, parallel implementation, and verification.
---

# Engineering Orchestration & Synthesis

## Process
1. **Alignment:** Execute clear requests immediately; ask 1–3 concise clarifying questions only when genuine architectural forks exist; write a formal plan only when explicitly requested.
2. **Recon:** Delegate read-only reconnaissance to `scout` and `researcher` to identify existing reusable utilities and partition the work into strictly non-overlapping file sets.
3. **Parallel Build:** Dispatch `backend`, `frontend`, and `fullstack` concurrently across disjoint file scopes. Once implementation and deterministic checks (`build`, `typecheck`, `lint`) pass, run `qa-reviewer` for an independent read-only code and security audit.
4. **Synthesis:** Present the uncommitted diff and verification evidence to the user. Never run `git commit`, `git push`, destructive commands, or dependency installations without explicit authorization.
