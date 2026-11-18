# AORG for Bloks

Native team and skill templates for [Bloks](https://github.com/hamedgitty/bloks), adapted from AORG's department packs. These are Bloks team files, not renamed OpenMausBot BotMRR manifests.

| Team | Members |
| :--- | ---: |
| [Amazon FBA & Seller Central Operations Crew](teams/amazon-ops.md) | 5 |
| [Personal Assistant and Career](teams/assistant.md) | 7 |
| [Workflow Automation & AI Systems Crew](teams/automation-ai.md) | 4 |
| [Business, Client & Agency Operations Crew](teams/business.md) | 4 |
| [Content Creation, Video & Production Crew](teams/content-creation.md) | 5 |
| [Software Engineering](teams/engineering.md) | 7 |
| [Engineering Review](teams/engineering-review.md) | 2 |
| [Sales, Lead Qualification & Outreach Crew](teams/sales-outreach.md) | 3 |
| [SEO, Content & Conversion Growth Crew](teams/seo-growth.md) | 4 |
| [Social Media & Content Engine Crew](teams/socials.md) | 4 |

## Install

Use **Customize > Catalogue** and its file/link import to review a team before adding it. Labels may vary by installed version. For all referenced skills to resolve together, point the catalogue source at this pack's `index.json`; see the [installation guide](docs/installation.md). A direct team-file import does not read neighboring skill folders and resolves `uses:` against the configured catalogue, so our custom skill IDs need that catalogue source or separate reviewed skill installation.

Bloks allows 2 to 8 members per team. The original nine engineering roles are preserved as Software Engineering (7) plus Engineering Review (2), not silently dropped or combined. Each file creates one room; legacy multi-room layouts and app connections are not imported. Routines are deliberately omitted rather than guessing local times, time zones, or recurrence behavior.

- [Installation](docs/installation.md)
- [Format and maintenance](docs/guide.md)
- [Generated catalogue index](index.json)
- [License and ACON provenance](LICENSE.md)

## Validation status

Targets upstream Bloks **3.2.9**, revision `672447623d105b0fb821eb9b34ec00f8473fb796`. The catalogue is built and checked using that revision's unmodified `buildIndex`, `parseTeamFile`, and `parseSkillFile` implementations. Static parser acceptance is not a live installation or proof of runtime delegation. No agents, accounts, routines, app connections, or running services are created by these repository files.
