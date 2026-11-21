# Install an OpenMausBot Team

This guide explains how to configure your default **Chief of Staff** and import any department team from `aorg/openmausbot` (such as [**`engineering`**](../teams/engineering/README.md), [**`assistant`**](../teams/assistant/README.md), or [**`content-creation`**](../teams/content-creation/README.md)).

---

## Step 1: Configure Your Default Chief of Staff

When you first install OpenMausBot, it creates a single default **Chief of Staff**.
1. Open your default Chief of Staff's **Bot settings -> Instructions**.
2. Paste the [**Default Chief of Staff Instructions**](../README.md#default-chief-of-staff-instructions) from `openmausbot/README.md`.
3. Under **Before acting**, choose **Ask me first** (or **Decide for me**).

*(Note: You do **not** need to manually paste instructions into imported team bots—OpenMausBot automatically populates each imported bot's instructions from its `team.md` file.)*

---

## Step 2: Import Any Department Team

### Method 1: OpenMausBot Desktop UI (`Teams -> Import`) — Recommended

Each team folder under [`teams/`](../teams/) includes a single-file BotMRR v1 `.md` playbook:
- **Software Engineering Crew (9 agents):** [`teams/engineering/team.md`](../teams/engineering/team.md)
- **Personal Assistant, MPOR & Job Scout Crew (11 agents):** [`teams/assistant/team.md`](../teams/assistant/team.md)
- **Content Creation, Video & Production Crew (5 agents):** [`teams/content-creation/team.md`](../teams/content-creation/team.md)
- **Amazon FBA & Seller Central Crew (5 agents):** [`teams/amazon-ops/team.md`](../teams/amazon-ops/team.md)
- **Social Media & Content Engine Crew (4 agents):** [`teams/socials/team.md`](../teams/socials/team.md)
- **Business, Client & Agency Ops Crew (4 agents):** [`teams/business/team.md`](../teams/business/team.md)
- **SEO, Content & Conversion Growth Crew (4 agents):** [`teams/seo-growth/team.md`](../teams/seo-growth/team.md)
- **Sales, Lead Qualification & Outreach Crew (3 agents):** [`teams/sales-outreach/team.md`](../teams/sales-outreach/team.md)
- **Workflow Automation & AI Systems Crew (4 agents):** [`teams/automation-ai/team.md`](../teams/automation-ai/team.md)

Steps:
1. Open **OpenMausBot** and navigate to **Teams -> Import**.
2. Select any `team.md` file from your local disk (or paste its raw GitHub URL).
3. Review the preview (Team Lead, specialist bots, shared rooms, playbooks, and paused routines) and click **Import**.

---

### Legacy compatibility and standalone skills

The `team.mausteam.json` files are retained for legacy importers. They do not automatically install the adjacent `skills/` folders. Current `openmausbot team apply` uses its own YAML/JSON team-file schema; these packs have not been converted to that schema.

The renamed `team.md` packages still use **BotMRR v1**, with embedded playbooks. A filename change is not a v2 conversion or proof of standalone skill installation. Use the **Import** tab; **From a folder** scouts a project and suggests bots rather than importing the defined roster.

---

## Step 3: Verify After Importing

1. **One Chief of Staff Only:** Your workspace keeps OpenMausBot's default **Chief of Staff** as the sole Chief of Staff, while each imported department is led by its own **Team Lead** (`tech-lead`, `concierge`, `showrunner`, etc.).
2. **Routines Start Paused:** All scheduled routines install with `enabledAfterInstall: false`. Enable only the ones you want active.
3. **Human Approval Gates:** No team will commit/push code, send emails, publish posts, or submit OnlineJobs.ph applications without your explicit confirmation.
