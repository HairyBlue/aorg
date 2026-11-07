# AORG — Agent Organization Collection

> **Reusable, ready-to-import AI agent organizations and department teams across agentic platforms.**

**AORG** (`aorg`) is a multi-platform repository of importable AI agent organizations and department teams grounded in the [**ACON (Agentic Conventions & Control Plane Network)**](https://github.com/HairyBlue/acon) standard (*"Talk to one agent. Ship with a crew."*).

Each platform folder follows the same clean `docs/` + `teams/` structure so you can import whichever department team you need.

---

## Supported & Planned Platforms

| Platform Directory | Status | Included Teams (`teams/`) | Documentation |
| :--- | :---: | :--- | :--- |
| [**`paperclip/`**](paperclip/README.md) | Ready | • [`paperclip-acon-team`](paperclip/teams/paperclip-acon-team/README.md) — 17-agent ACON organization | [Guide](paperclip/docs/guide.md) · [Installation](paperclip/docs/installation.md) |
| [**`openmausbot/`**](openmausbot/README.md) | Ready | • [**`engineering`**](openmausbot/teams/engineering/README.md) — 9-agent Software Engineering Crew<br>• [**`assistant`**](openmausbot/teams/assistant/README.md) — 6-agent Personal Assistant + **MPOR Reporter** + **OnlineJobs.ph Job Scout**<br>• [**`content-creation`**](openmausbot/teams/content-creation/README.md) — 5-agent Content Creation, Video & Production Crew<br>• [**`amazon-ops`**](openmausbot/teams/amazon-ops/README.md) — 5-agent Amazon FBA & Seller Central Crew<br>• [**`socials`**](openmausbot/teams/socials/README.md) — 4-agent Social Media & Content Repurposing Crew<br>• [**`business`**](openmausbot/teams/business/README.md) — 4-agent Business, SOP & Client Operations Crew<br>• [**`seo-growth`**](openmausbot/teams/seo-growth/README.md) — 4-agent SEO, Content & Conversion Growth Crew<br>• [**`sales-outreach`**](openmausbot/teams/sales-outreach/README.md) — 3-agent B2B Lead Qualification & Outreach Crew<br>• [**`automation-ai`**](openmausbot/teams/automation-ai/README.md) — 4-agent n8n / Make / Zapier & AI Workflow Crew | [Guide](openmausbot/docs/guide.md) · [Installation](openmausbot/docs/installation.md) |
| `codync/` *(planned)* | Planned | Reserved for Codync agent organizations | — |
| `grokbot/` *(planned)* | Planned | Reserved for Grokbot agent organizations | — |

---

## Repository Structure

```text
aorg/
├── README.md                                     # Multi-platform index & overview
├── LICENSE                                       # MIT License + ACON provenance notice
├── openmausbot/                                  # OpenMausBot agent organization collection
│   ├── README.md
│   ├── docs/
│   │   ├── guide.md
│   │   └── installation.md
│   └── teams/
│       ├── amazon-ops/                           # 5-agent Amazon FBA & Seller Central Crew
│       ├── assistant/                            # 6-agent Personal Assistant + MPOR + OnlineJobs.ph Crew
│       ├── automation-ai/                        # 4-agent n8n / Make / Zapier & AI Workflow Crew
│       ├── business/                             # 4-agent Business, SOP & Client Ops Crew
│       ├── content-creation/                     # 5-agent Content Creation, Video & Production Crew
│       ├── engineering/                          # 9-agent Software Engineering Crew
│       ├── sales-outreach/                       # 3-agent Lead Qualification & Cold Outreach Crew
│       ├── seo-growth/                           # 4-agent SEO, Content & CRO Growth Crew
│       └── socials/                              # 4-agent Social Media & Content Engine Crew
└── paperclip/                                    # Paperclip agent organization collection
    ├── README.md
    ├── docs/
    │   ├── guide.md
    │   └── installation.md
    └── teams/
        └── paperclip-acon-team/                  # 17-agent ACON organization for Paperclip
```

---

## License

Released under the [MIT License](LICENSE).
