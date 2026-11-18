# Bloks format and maintenance

## Layout

```text
bloks/
  README.md
  LICENSE.md
  docs/
  index.json
  teams/<id>.md
  skills/<id>/SKILL.md
```

Bloks' catalogue requires `teams/<id>.md`, not the OpenMausBot `teams/<id>/team.md` layout. There are no duplicate uppercase `TEAM.md` rosters or legacy JSON manifests in this integration.

Team files have flat `name`, `blurb`, `tags`, `author`, and `version` fields followed by one `## Role` section per member. Each member has a name suggestion, seniority, appearance, short skill lines, and explicit `uses:` skill IDs. Exactly one member has seniority 5 in every team. No engine, API key, browser, external app, or tool-server configuration is embedded.

Skills keep their detailed AORG workflows, including the separate general-progress and MPOR/SPOR reporting policies. Their frontmatter uses standard Agent Skills fields plus Bloks metadata. Every skill states when to use it, a numbered entry step, what it is not for, the expected result, and its approval boundary. Reporting examples remain illustrative, never audited accomplishments.

The engineering build and review teams are separate rooms. Cross-room handoff availability must be checked in the installed app; these files do not guarantee cross-room delegation. A missing independent review must be disclosed, not simulated by the writer.

## Rebuild the index

No scripts are bundled with this integration. The root `index.json` keeps item paths relative to `bloks/`, so `teams/<id>.md` and `skills/<id>/SKILL.md` resolve without a `catalog/` directory.

When templates change, regenerate the index using `buildIndex` and `serializeIndex` from a separate trusted checkout of the pinned Bloks source. Pass the files under this integration's `teams/` and `skills/`, with paths relative to `bloks/`. The upstream builder validates the files and skill references and calculates exact byte lengths and SHA-256 fingerprints. Never hand-edit fingerprints. Bump versions when changing published items.

## Sources

- [Upstream catalogue format](https://github.com/hamedgitty/bloks/blob/672447623d105b0fb821eb9b34ec00f8473fb796/catalog/README.md)
- [Team parser and limits](https://github.com/hamedgitty/bloks/blob/672447623d105b0fb821eb9b34ec00f8473fb796/server/team-file.ts)
- [Catalogue and skill parser](https://github.com/hamedgitty/bloks/blob/672447623d105b0fb821eb9b34ec00f8473fb796/server/catalog.ts)

Templates are adapted from AORG, not copied from Bloks' built-in teams. Upstream application source is not redistributed here. The pack's license preserves the source-specific ACON notice.
