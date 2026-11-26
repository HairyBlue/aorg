# AORG — Paperclip Teams (`aorg/paperclip`)

A collection of reusable, ready-to-import AI agent teams and organization templates for **Paperclip**.

Each organization is kept as a portable team package under [`teams/`](teams/). Its first team is the [Paperclip ACON team](teams/paperclip-acon-team/README.md), a reusable 17-agent roster with standalone instructions and its own package-specific support and license documents.

## Start here

- [Install the first team](docs/installation.md)
- [Use and extend Paperclip teams](docs/guide.md)
- [First-team roster](teams/paperclip-acon-team/TEAM.md)
- [First-team validation and limits](teams/paperclip-acon-team/VALIDATION.md)
- [Repository license](../LICENSE) and [first-team license/provenance](teams/paperclip-acon-team/LICENSE.md)

## Directory layout

```text
teams/paperclip-acon-team/  First importable organization package
  .paperclip.yaml           Package manifest
  COMPANY.md                Organization and roster data
  agents/<role>/AGENTS.md   17 standalone role instructions
  README.md, TEAM.md,
  VALIDATION.md, LICENSE.md  Team-specific guidance and notices
docs/                       Installation and general maintainer/user guides
```

The team files are kept at the archive root: when distributing a team ZIP, include `.paperclip.yaml`, `COMPANY.md`, `agents/`, and the four support documents directly, not an extra enclosing repository directory.

## Shared Skill References

- `business/sop-and-process-builder` Reference Case 1 (E-Commerce Customer Support SOP & Miro Decision-Tree): [`openmausbot/teams/business/skills/sop-and-process-builder/references/case-1/README.md`](../openmausbot/teams/business/skills/sop-and-process-builder/references/case-1/README.md) (synced from ACON `.agents/skills/business/sop-and-process-builder/references/case-1/README.md`).
