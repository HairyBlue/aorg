# T3 Code Installation & Quickstart

## 1. Clone `aorg` Anywhere
Clone `aorg` to any local folder (for example `~/aorg` or `~/ai-stuff/aorg`). All paths inside `t3code/roster.json` are **relative to your `aorg` folder**, so anyone can use this setup on any machine.

*(Optional)* If you also use **ACON**, install ACON skills into `~/.gemini/config/skills/` (or `.agents/skills/`).

---

## 2. Start Your Global Orchestrator ("No Project" Thread)

Open a **"No Project"** thread in T3 Code and paste (replace `<AORG_ROOT>` with your local `aorg` path):

```text
Initialize as the Global Orchestrator for my T3 Code workspace.
My aorg folder is at <AORG_ROOT>.
Read <AORG_ROOT>/t3code/ORCHESTRATOR.md and <AORG_ROOT>/t3code/roster.json.
Confirm you are ready without taking external actions.
```

---

## 3. Bootstrap a New Project (Assign a Head + Invite Bots)

From your **Global Orchestrator** thread (or from the first thread inside a new project), tell it what the project is for:

### Example A: Web App + SEO Project
```text
Project: Davao del Sur Website
Goal: Laravel + Blade website with technical SEO and content optimization.
Invite a Project Head (tech-lead) plus frontend, backend, devops-guard, qa-reviewer, growth-lead, tech-seo, and content-writer from t3code/roster.json.
```

### Example B: Engineering Starter Team
```text
For this project, invite the engineering starter preset (tech-lead, scout, frontend, backend, qa-reviewer) from t3code/roster.json.
```

### Example C: Invite One Specific Bot Later
```text
Invite devops-guard to this project from t3code/roster.json.
```
