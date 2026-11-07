---
name: parallel-crew-dispatch
description: Split work across multiple concurrent Backend, Frontend, and Full-Stack engineers with zero file collisions.
---

# Cross-Layer & Intra-Layer Parallel Dispatch

## Use this when

A feature, refactor, or bug fix spans 2 or more non-overlapping file scopes across backend, frontend, or multiple modules within the same layer.

## Process

1. **Map File Boundaries First:** Have `scout` list every target file and classify shared entry points (`App.tsx`, router registries, barrel exports, root providers).
2. **Cross-Layer Parallelism:** When work touches both backend and frontend, dispatch `backend` (routes, services, schema) and `frontend` (pages, components, styles) concurrently.
3. **Intra-Layer Parallelism (2+ Frontend or 2+ Backend Engineers):** When a pure frontend or pure backend task touches independent pages, components, endpoints, or services, dispatch `frontend` + `fullstack` (2 concurrent frontend slices) or `backend` + `fullstack` (2 concurrent backend slices) on strictly disjoint file sets.
4. **Synthesis Slice:** Keep shared wiring files out of the parallel slices; assign `fullstack` to wire the shared entry point after parallel slices finish and run full `build`, `typecheck`, and `lint` verification.

## Output

Use: Parallel Slice Matrix (Engineer, Owned Files, Excluded Shared Files), Synthesis Step, and Deterministic Verification Result.

## Guardrails

No two concurrent workers may edit the same file. Never funnel multi-file, non-conflicting work through a single sequential engineer when parallel crew members can execute simultaneously.
