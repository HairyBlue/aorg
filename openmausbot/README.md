# AORG — OpenMausBot Teams (`aorg/openmausbot`)

Ready-to-import AI agent teams and department groups for [**OpenMausBot**](https://openmausbot.com).

> **Architecture — One Global Chief of Staff + Department Team Leads:**  
> OpenMausBot creates a single default **Chief of Staff** when you set up your workspace. Each imported team below uses a **Team Lead** (not a duplicate Chief of Staff) so your workspace stays clean with **only one Chief of Staff** at the top.

---

## Available Teams (`teams/`)

Each folder under [`teams/`](teams/) is a self-contained department team you can import independently into OpenMausBot:

| Team Folder | Agents | Team Lead | Purpose & Roster | Import File (`.md`) |
| :--- | :---: | :--- | :--- | :--- |
| [**`teams/engineering/`**](teams/engineering/README.md) | 9 | `tech-lead` (*Tech Lead*) | **Software Engineering Crew:** Parallel `backend`, `frontend`, and `fullstack` engineers (cross-layer & intra-layer), `scout`, `researcher`, `architect`, `qa-reviewer` (Code & OWASP Security), and `devops-guard`. | [`teams/engineering/team.md`](teams/engineering/team.md) |
| [**`teams/assistant/`**](teams/assistant/README.md) | 11 | `concierge` (*Concierge*) | **Personal Assistant, MPOR & Job Scout Crew:** Daily priority planner (`concierge`), **OnlineJobs.ph & Remote Job Scout (`job-scout`)**, **MPOR/SPOR Reporter (`mpor-reporter`)**, **Daily Progress Reporter (`daily-progress-reporter`)**, `inbox-triage`, `second-brain` (Obsidian/Notion notes), and `admin-ops` (exam/device maintenance logger). | [`teams/assistant/team.md`](teams/assistant/team.md) |
| [**`teams/content-creation/`**](teams/content-creation/README.md) | 5 | `showrunner` (*Showrunner*) | **Content Creation, Video & Production Crew:** Covers talking-head videos, YouTube long-form, screen tutorials, Shorts/Reels, carousels, and optional AI clips (`script-writer`, `visual-director` for A-roll/B-roll or AI prompts, `edit-producer`, and `growth-packager`). | [`teams/content-creation/team.md`](teams/content-creation/team.md) |
| [**`teams/amazon-ops/`**](teams/amazon-ops/README.md) | 5 | `seller-lead` (*Seller Lead*) | **Amazon FBA & Seller Central Crew:** `product-scout` (ASIN & margin research), `listing-seo` (titles, 5 bullets, A+ & backend keywords), `ppc-analyst` (ACOS/TACOS & negative keywords), and `inventory-ops` (FBA restock & review root causes). | [`teams/amazon-ops/team.md`](teams/amazon-ops/team.md) |
| [**`teams/socials/`**](teams/socials/README.md) | 4 | `editor-in-chief` (*Editor in Chief*) | **Social Media & Content Engine Crew:** `trend-radar` (hooks & angles), `repurposer` (1 asset -> X thread, LinkedIn, IG/FB, Short/Reel script), and `community-desk` (comment & DM reply drafts). | [`teams/socials/team.md`](teams/socials/team.md) |
| [**`teams/business/`**](teams/business/README.md) | 4 | `ops-director` (*Ops Director*) | **Business, Client & Agency Ops Crew:** `sop-architect` (Loom/notes -> step-by-step SOPs), `client-success` (onboarding, weekly updates, scope guard), and `market-intel` (competitor & subscription spend audit). | [`teams/business/team.md`](teams/business/team.md) |
| [**`teams/seo-growth/`**](teams/seo-growth/README.md) | 4 | `growth-lead` (*Growth Lead*) | **SEO, Content & Conversion Growth Crew:** `keyword-mapper` (intent clusters & striking-distance pages), `tech-seo` (indexing, schema, internal links & CRO), and `content-writer` (articles & landing pages). | [`teams/seo-growth/team.md`](teams/seo-growth/team.md) |
| [**`teams/sales-outreach/`**](teams/sales-outreach/README.md) | 3 | `revenue-lead` (*Revenue Lead*) | **Sales, Lead Qualification & Outreach Crew:** `lead-miner` (ICP & buying-signal scoring) and `outreach-closer` (context-first cold emails/DMs & stalled thread recovery). | [`teams/sales-outreach/team.md`](teams/sales-outreach/team.md) |
| [**`teams/automation-ai/`**](teams/automation-ai/README.md) | 4 | `automation-architect` (*Automation Architect*) | **Workflow Automation & AI Systems Crew:** `process-mapper` (Trigger -> Action specs), `workflow-builder` (idempotent n8n, Make, Zapier & webhooks), and `prompt-qa` (strict JSON schemas & LLM node testing). | [`teams/automation-ai/team.md`](teams/automation-ai/team.md) |

---

## Default Chief of Staff Instructions

OpenMausBot creates a single default **Chief of Staff** out of the box. While each imported department bot gets its own instructions automatically on import, you can paste the following block into your default Chief of Staff's **Bot settings -> Instructions** so it knows how to work whether you have 0, 1, or multiple department teams installed:

```text
You are the single global Chief of Staff for this workspace. Communicate concisely, directly, and outcome-first—no corporate filler or generic AI openings.

1. Delegate-First Team & Specialist Coordination:
   - Check which teams, rooms, or specialist agents are currently available in this workspace.
   - Always ask the matching team's lead or specialist agent to perform the task (and run independent tasks in parallel when work does not overlap), including naming which skills to use.
   - Only handle a task directly yourself if no matching specialist is available OR the user explicitly specifies that only you should do it.

2. Pragmatic Execution:
   - Execute clear requests immediately; ask 1–3 brief clarifying questions only when genuine ambiguity exists.
   - Keep solutions simple and minimal (YAGNI, reuse existing code/workflows, prefer standard tools over unnecessary dependencies).
   - For coding tasks, verify changes using deterministic build, typecheck, and lint checks; do not write unrequested test suites unless explicitly asked.

3. Strict Approval Gate:
   - Never run git commit, git push, destructive commands, or install new dependencies without explicit user approval.
   - Never send external emails/messages, publish posts, change ad spend, or submit job applications automatically—always present drafts for confirmation first.
```

---

## Bot Avatar Shapes & Colors (`Bot` Picker Guide)

When you import a `team.md` file, OpenMausBot automatically sets each bot's **color** from the file (`green`, `blue`, `red`, `orange`, `purple`, `cyan`, `pink`, `yellow`), while defaulting the mascot shape to **#1 Cursor**.

If you want each bot to have a distinct shape in the **Bot Avatar Picker** (Row 1 = `#1–#5`, Row 2 = `#6–#10`), here is the recommended mapping:

| Archetype / Role | Recommended Shape (in Picker) | Color | Example Bots |
| :--- | :--- | :--- | :--- |
| **Global Chief of Staff** | **#10 Star** (Row 2, Col 5) | **Purple** or **Yellow** | Default Chief of Staff |
| **Department Team Leads** | **#1 Cursor / Pointer** (Row 1, Col 1) | **Purple** / **Green** / **Orange** | `tech-lead`, `concierge`, `showrunner`, `seller-lead`, `editor-in-chief`, `ops-director`, `growth-lead`, `revenue-lead`, `automation-architect` |
| **Scouts, Researchers & Miners** | **#9 Diamond** (Row 2, Col 4) | **Blue** | `scout`, `job-scout`, `product-scout`, `trend-radar`, `keyword-mapper`, `lead-miner` |
| **Architects, Strategists & Planners** | **#8 Hexagon** (Row 2, Col 3) | **Yellow** | `architect`, `researcher`, `ppc-analyst`, `market-intel`, `process-mapper` |
| **Backend, Technical & Workflow Builders** | **#4 Square** (Row 1, Col 4) | **Green** | `backend`, `workflow-builder`, `tech-seo`, `sop-architect`, `admin-ops` |
| **Frontend, Visuals, Writers & Repurposers** | **#6 Teardrop** (Row 2, Col 1) | **Cyan** | `frontend`, `visual-director`, `script-writer`, `repurposer`, `listing-seo`, `content-writer` |
| **Full-Stack, Editors & Closers** | **#5 Pill / Capsule** (Row 1, Col 5) | **Orange** | `fullstack`, `edit-producer`, `outreach-closer`, `client-success` |
| **QA, Security, Guards & Inventory** | **#7 Gumdrop / Shield** (Row 2, Col 2) | **Red** | `qa-reviewer`, `devops-guard`, `prompt-qa`, `inventory-ops` |
| **MPOR Reporting, Packaging & Inbox/Community** | **#3 Circle** (Row 1, Col 3) | **Pink** | `mpor-reporter`, `growth-packager`, `community-desk`, `inbox-triage`, `second-brain` |

---

## How to Import a Team into OpenMausBot

### 1. OpenMausBot Desktop (`Teams -> Import`) — Fastest
1. In OpenMausBot, open **Teams -> Import**.
2. Select any team's `team.md` file under [`teams/<team>/team.md`](teams/) (or paste its raw GitHub URL).
3. Review the preview and click **Import**.

### 2. Give the Blueprint to Your Default Chief of Staff
Attach any `team.md` file directly in chat with your default Chief of Staff.

### 3. Legacy compatibility and skills

Each folder retains `team.mausteam.json` for legacy importers. The current CLI's YAML/JSON team-file schema is different; do not assume `team apply <directory>` accepts this legacy pack.

The lowercase `team.md` packages currently retain **BotMRR v1**. Renaming them does not convert them to v2 or automatically install adjacent standalone skills. Use the **Import** flow, not the **From a folder** project-scouting tab.

---

## Documentation

- [**Installation Guide (`docs/installation.md`)**](docs/installation.md) — Step-by-step UI, Chief of Staff instruction setup, and CLI import instructions.
- [**Team Guide (`docs/guide.md`)**](docs/guide.md) — Overview of all 9 department teams and how to add more.
