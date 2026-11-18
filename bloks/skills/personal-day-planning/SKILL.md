---
name: personal-day-planning
description: Turn messy brain dumps, schedules, and device/exam admin tasks into a calm Top-3 daily plan and verified ops log.
license: MIT
metadata:
  title: Personal Day Planning & Non-Coding Ops Log
  version: "1"
  author: AORG
  tags: assistant, workflow
---

Use this when the user needs to turn messy brain dumps, schedules, and device/exam admin tasks into a calm Top-3 daily plan and verified ops log.

1. Confirm the requested scope and available evidence, then follow the workflow below. Reuse answers already supplied.

# Personal Day Planning & Non-Coding Ops Log

## Use this when

The user wants a morning briefing, turns a brain dump into a daily action list, or logs non-coding operational work such as exam assistance or lab/device maintenance.

## Process

1. **Brain-Dump to Top-3 Plan:** Group incoming tasks into **Must-Do Today (max 3)**, **Next Up**, and **Waiting On**, checking any connected calendar or local notes for time blocks and deadlines.
2. **Non-Coding Admin & Device Ops Logging:** When the user mentions exam assistance, lab/device maintenance, hardware/network fixes, or office admin work, record the exact date, task description, confirmed unit count, and category so `mpor-reporter` has verified non-coding evidence ready for daily and monthly MPOR reports.

## Output

Use: Top-3 Priorities Today, Schedule / Deadlines, Logged Admin/Device Ops (Date, Task, Confirmed Units), and Waiting On / Follow-Ups.

## Guardrails

Never fabricate dates or unit quantities for non-coding work; keep unconfirmed quantities marked `Pending`.

Not for: Acting outside the requested scope or presenting unverified work as completed.
Return: The requested draft or result, supporting evidence where relevant, and any unresolved assumptions or blockers.
Approval: Ask before sending, publishing, purchasing, booking, cancelling, deleting, changing live systems, installing dependencies, committing or pushing, or enabling recurring automation. Drafts and reviews alone do not authorize those actions.
