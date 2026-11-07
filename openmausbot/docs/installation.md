# Install an OpenMausBot Team

This guide explains how to configure your default **Chief of Staff** and import any department team from `aorg/openmausbot` (such as [**`engineering`**](../teams/engineering/README.md), [**`assistant`**](../teams/assistant/README.md), or [**`content-creation`**](../teams/content-creation/README.md)).

---

## Step 1: Configure Your Default Chief of Staff

When you first install OpenMausBot, it creates a single default **Chief of Staff**.
1. Open your default Chief of Staff's **Bot settings -> Instructions**.
2. Paste the [**Default Chief of Staff Instructions**](../README.md#default-chief-of-staff-instructions) from `openmausbot/README.md`.
3. Under **Before acting**, choose **Ask me first** (or **Decide for me**).

*(Note: You do **not** need to manually paste instructions into imported team bots—OpenMausBot automatically populates each imported bot's instructions from its `<team>.md` file.)*

---

## Step 2: Import Any Department Team

### Method 1: OpenMausBot Desktop UI (`Teams -> Import`) — Recommended

Each team folder under [`teams/`](../teams/) includes a single-file BotMRR v1 `.md` playbook:
- **Software Engineering Crew (9 agents):** [`teams/engineering/engineering.md`](../teams/engineering/engineering.md)
- **Personal Assistant, MPOR & OnlineJobs.ph Crew (6 agents):** [`teams/assistant/assistant.md`](../teams/assistant/assistant.md)
- **Content Creation, Video & Production Crew (5 agents):** [`teams/content-creation/content-creation.md`](../teams/content-creation/content-creation.md)
- **Amazon FBA & Seller Central Crew (5 agents):** [`teams/amazon-ops/amazon-ops.md`](../teams/amazon-ops/amazon-ops.md)
- **Social Media & Content Engine Crew (4 agents):** [`teams/socials/socials.md`](../teams/socials/socials.md)
- **Business, Client & Agency Ops Crew (4 agents):** [`teams/business/business.md`](../teams/business/business.md)
- **SEO, Content & Conversion Growth Crew (4 agents):** [`teams/seo-growth/seo-growth.md`](../teams/seo-growth/seo-growth.md)
- **Sales, Lead Qualification & Outreach Crew (3 agents):** [`teams/sales-outreach/sales-outreach.md`](../teams/sales-outreach/sales-outreach.md)
- **Workflow Automation & AI Systems Crew (4 agents):** [`teams/automation-ai/automation-ai.md`](../teams/automation-ai/automation-ai.md)

Steps:
1. Open **OpenMausBot** and navigate to **Teams -> Import**.
2. Select any `<team>.md` file from your local disk (or paste its raw GitHub URL).
3. Review the preview (Team Lead, specialist bots, shared rooms, playbooks, and paused routines) and click **Import**.

---

### Method 2: CLI Compatibility Directory (`openmausbot team apply`)

```bash
openmausbot team apply /path/to/aorg/openmausbot/teams/engineering
openmausbot team apply /path/to/aorg/openmausbot/teams/assistant
```

---

## Step 3: Verify After Importing

1. **One Chief of Staff Only:** Your workspace keeps OpenMausBot's default **Chief of Staff** as the sole Chief of Staff, while each imported department is led by its own **Team Lead** (`tech-lead`, `concierge`, `showrunner`, etc.).
2. **Routines Start Paused:** All scheduled routines install with `enabledAfterInstall: false`. Enable only the ones you want active.
3. **Human Approval Gates:** No team will commit/push code, send emails, publish posts, or submit OnlineJobs.ph applications without your explicit confirmation.
