# T3 Code Crew Guide

## Architecture: Clean Repos, Persistent Bot Threads

In T3 Code, every project is a workspace group—similar to rooms/channels in OpenMausBot—where each bot is a **top-level thread** you can talk to directly or coordinate through a Head.

```text
[Global Orchestrator]  ("No Project" thread — reads ORCHESTRATOR.md + roster.json)
   ├── Project: Davao del Sur Website
   │     ├── Tech Lead (Project Head)
   │     ├── Frontend
   │     ├── Backend
   │     ├── QA Reviewer
   │     ├── DevOps Guard
   │     ├── Growth Lead
   │     ├── Tech SEO
   │     └── Content Writer
   └── Project: Personal Ops / t3-assistant
         ├── Concierge (Project Head)
         ├── MPOR Reporter
         └── Job Scout
```

### Why a Central Registry?
- Client and code repositories (e.g., `Davao del Sur Website`) stay **100% clean**—no bot prompts or skill folders copied into them.
- All 49 bot personalities live in `<AORG_ROOT>/t3code/teams/<team>/bots/<bot>.md`.
- All shared ACON skills live in `~/.gemini/config/skills/` (optional) and team playbooks live in `<AORG_ROOT>/openmausbot/teams/<team>/skills/`.
- Every spawned thread inherits your **project's default model and runtime mode** (`inherit`).

---

## Mixing Bots Across Teams

Projects rarely fit a single department. You can invite bots from multiple teams into the same T3 Code project:
- **Website + SEO Project:** `tech-lead`, `frontend`, `backend`, `qa-reviewer`, `devops-guard` + `growth-lead`, `tech-seo`, `content-writer`.
- **SaaS + Growth Project:** `engineering` starter + `seo-growth` + `sales-outreach`.
- **Agency Client Project:** `ops-director`, `client-success` + `tech-lead` + `growth-lead`.

---

## Managing Active Bots

- **Invite more bots anytime:** Ask the Global Orchestrator or your Project Head: *"Invite `qa-reviewer` and `devops-guard` to this project."*
- **Avoid duplicates:** The Orchestrator/Head checks `t3_thread_list` before calling `create_threads`.
- **Switch a bot's model anytime:** Use T3 Code's thread model selector on any individual bot thread if you want a heavier or lighter model for that specific role.
