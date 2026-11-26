# OpenMausBot Personal Assistant & Career Pack (`assistant`)

An importable 9-agent Personal Assistant, Daily Progress/Kanban Reporting, MPOR/SPOR Reporting, and OnlineJobs.ph Career Scout team for **OpenMausBot**, led by **Concierge (`concierge`)**.

## Contents

- [`team.md`](team.md) — **BotMRR v1 single-file import package.** Import directly in OpenMausBot via **Teams -> Import**, or give it to your Chief of Staff in chat.
- [`team.mausteam.json`](team.mausteam.json) — Legacy compatibility manifest (`openmaus.team` v1); does not bundle standalone skills.
- [`skills/`](skills/) — Standalone skill files (`personal-day-planning`, `inbox-and-notes-triage`, `job-hunt-onlinejobs`, `daily-progress-report`, `mpor-progress-report`).
- [`LICENSE.md`](LICENSE.md) — MIT license.

## Reporting routes

- **Daily Progress Reporter:** General daily, weekly, monthly, or custom updates and optional paste-ready Trello/Kanban card copy. Drafts in chat; no mandatory file path or MPOR columns.
- **MPOR Reporter:** Prescribed workplace MPOR/SPOR forms, selected expected-output rows, and progress-based draft counts with supporting breakdowns. Follows office-defined date ranges rather than forcing four monthly buckets.
- Both share one user-approved accomplishment inventory, count progress rather than commits, respect excluded categories, and distinguish OT plans from confirmed completed work. Worked examples are included in the skills and import package.

Daily check-ins belong to `daily-progress-reporter`; Friday office-report rollups remain with `mpor-reporter`. All four routines remain paused until explicitly enabled. This update changes the import files only; it does not install bots, enable routines, or publish reports.
