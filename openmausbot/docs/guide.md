# OpenMausBot Teams Guide

`aorg/openmausbot` organizes multi-agent departments into clean **department folders** under [`teams/`](../teams/).

## 1. Architecture: One Chief of Staff + Department Team Leads

OpenMausBot creates a single default **Chief of Staff** when you initialize your workspace. To prevent duplicate Chiefs of Staff when importing multiple departments, none of the department packs declare `chiefOfStaff` in their YAML frontmatter. Instead, each department has its own **Team Lead** (`defaultResponder` in its primary room):

| Department Team | Agents | Team Lead | Primary Focus |
| :--- | :---: | :--- | :--- |
| [**`engineering`**](../teams/engineering/README.md) | 9 | `tech-lead` (*Tech Lead*) | Parallel software engineering (`backend`, `frontend`, `fullstack`), codebase scouting (`scout`, `researcher`), architecture (`architect`), code/security audit (`qa-reviewer`), and git/release safety (`devops-guard`). |
| [**`assistant`**](../teams/assistant/README.md) | 9 | `concierge` (*Concierge*) | Daily priority planning, **MPOR/SPOR forms (`mpor-reporter`) and general progress/Kanban drafts (`daily-progress-reporter`)**, **OnlineJobs.ph & Remote Job Scout (`job-scout`)**, inbox triage (`inbox-triage`), Second Brain notes (`second-brain`), and non-coding exam/device maintenance logging (`admin-ops`). |
| [**`content-creation`**](../teams/content-creation/README.md) | 5 | `showrunner` (*Showrunner*) | Talking-head videos, YouTube long-form, screen-recorded tutorials, Shorts/Reels/TikToks, carousels, and optional AI short-clips (`script-writer`, `visual-director`, `edit-producer`, `growth-packager`). |
| [**`amazon-ops`**](../teams/amazon-ops/README.md) | 5 | `seller-lead` (*Seller Lead*) | Amazon FBA product research (`product-scout`), listing SEO & A+ copy (`listing-seo`), PPC bid/ACOS optimization (`ppc-analyst`), and FBA restock planning (`inventory-ops`). |
| [**`socials`**](../teams/socials/README.md) | 4 | `editor-in-chief` (*Editor in Chief*) | Trend/hook scouting (`trend-radar`), 1-to-many asset repurposing (`repurposer`), and comment/DM reply drafting (`community-desk`). |
| [**`business`**](../teams/business/README.md) | 4 | `ops-director` (*Ops Director*) | SOP authoring (`sop-architect`), client onboarding & weekly status briefs (`client-success`), and competitor/subscription spend audits (`market-intel`). |
| [**`seo-growth`**](../teams/seo-growth/README.md) | 4 | `growth-lead` (*Growth Lead*) | Keyword cluster mapping (`keyword-mapper`), technical SEO & CRO triage (`tech-seo`), and search-intent content writing (`content-writer`). |
| [**`sales-outreach`**](../teams/sales-outreach/README.md) | 3 | `revenue-lead` (*Revenue Lead*) | ICP lead mining (`lead-miner`) and context-first cold outreach + stalled thread follow-ups (`outreach-closer`). |
| [**`automation-ai`**](../teams/automation-ai/README.md) | 4 | `automation-architect` (*Automation Architect*) | Trigger-Action process mapping (`process-mapper`), idempotent n8n/Make/Zapier/webhook builds (`workflow-builder`), and LLM prompt/schema QA (`prompt-qa`). |

---

## 2. Adding or Customizing Teams

Each team folder under `teams/<team-name>/` is self-contained and includes:
- `team.md` — BotMRR v1 single-file Markdown playbook (`botmrr: 1`) for **Teams -> Import** in OpenMausBot Desktop.
- `team.mausteam.json` — Legacy compatibility manifest. `skills/<skill>/SKILL.md` contains standalone skills; these are not automatically installed by the legacy JSON manifest.
- `README.md` — Installation summary; the roster, shared rooms, and paused routines are defined in `team.md`.

Keep all routines paused by default (`enabledAfterInstall: false`), use a **Team Lead** instead of `chiefOfStaff` in department files, and never embed credentials or private tokens.
