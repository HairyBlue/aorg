# AORG — T3 Code Agent Organization (`aorg/t3code`)

A **T3 Code-native** multi-project, multi-bot organization grounded in **ACON** (`~/.gemini/config/skills/`).

Instead of copying bot prompts and skills into every repository, `aorg/t3code/` acts as a **central registry**:
- **Global Orchestrator ("No Project" thread):** Oversees all projects, creates Project Heads, and invites bots across projects.
- **Per-Project Head:** Each project gets a Team Head (e.g., `Tech Lead`, `Growth Lead`, `Concierge`) that knows what the project is for and spawns/coordinates the right specialist threads.
- **Invite-on-Demand Bot Threads:** Invite any combination of the **49 bots across 9 teams** into a project as top-level T3 Code threads (`create_threads`), inheriting the project's default model and runtime mode—without polluting your project repo.

---

## Available Teams (`teams/`)

| Team | Bots | Team Head | Purpose | Directory |
| :--- | :---: | :--- | :--- | :--- |
| `engineering` | 9 | `tech-lead` (*Tech Lead*) | Software engineering, parallel frontend/backend/fullstack, QA & OWASP review, DevOps/git safety | [`teams/engineering/`](teams/engineering/README.md) |
| `seo-growth` | 4 | `growth-lead` (*Growth Lead*) | Keyword intent mapping, technical SEO & CRO audits, SEO content briefs & copy | [`teams/seo-growth/`](teams/seo-growth/README.md) |
| `assistant` | 7 | `concierge` (*Concierge*) | Day planning, MPOR/SPOR, daily progress/Kanban, inbox triage, second brain, admin ops, job scout | [`teams/assistant/`](teams/assistant/README.md) |
| `business` | 4 | `ops-director` (*Ops Director*) | SOPs, client onboarding/scope guard, competitor & subscription spend audits | [`teams/business/`](teams/business/README.md) |
| `content-creation` | 5 | `showrunner` (*Showrunner*) | Scripts, storyboards/visual direction, edit timelines, thumbnails & titles | [`teams/content-creation/`](teams/content-creation/README.md) |
| `socials` | 4 | `editor-in-chief` (*Editor in Chief*) | Trend radar, multi-platform repurposing, community & DM reply drafts | [`teams/socials/`](teams/socials/README.md) |
| `amazon-ops` | 5 | `seller-lead` (*Seller Lead*) | ASIN/margin research, listing SEO, PPC wasted-spend audits, FBA restock & reviews | [`teams/amazon-ops/`](teams/amazon-ops/README.md) |
| `sales-outreach` | 3 | `revenue-lead` (*Revenue Lead*) | ICP lead qualification, context-first cold outreach, stalled thread recovery | [`teams/sales-outreach/`](teams/sales-outreach/README.md) |
| `automation-ai` | 4 | `automation-architect` (*Automation Architect*) | Process-to-automation specs, n8n/Make/Zapier/webhooks, structured LLM node QA | [`teams/automation-ai/`](teams/automation-ai/README.md) |

---

## Documentation

- [**Guide (`docs/guide.md`)**](docs/guide.md) — How the Global Orchestrator, Project Heads, and bot invites work together.
- [**Installation & Quickstart (`docs/installation.md`)**](docs/installation.md) — Copy-paste prompts to start your "No Project" Orchestrator and bootstrap any project.
- [**Machine-Readable Roster (`roster.json`)**](roster.json) — Index of all teams, heads, presets, bot prompt paths, and ACON skill paths.
