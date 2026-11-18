# Install an AORG team in Bloks

## Recommended: use the AORG catalogue source

1. Obtain this repository locally. These changes must be published separately before any new GitHub links can work.
2. In the installed app, open **Customize > Catalogue** and locate its catalogue source setting. Point it at an HTTPS URL serving `bloks/index.json`, or a loopback HTTP URL for local review. Source-setting placement may vary by version.
3. For a local preview, you can explicitly start a static server in a terminal:

   ```bash
   python3 -m http.server 8765 --bind 127.0.0.1 --directory /path/to/aorg/bloks
   ```

   Use `http://127.0.0.1:8765/index.json` as the source. Keep the server running while reviewing or installing, and stop it with Ctrl+C afterward. Do not bind to all interfaces or expose private folders. On a remote Bloks server, loopback means that server, not your laptop.
4. Review the team, every attached skill, member roles, and requested changes. Add it only after confirming the preview. Switching catalogue source changes what is browsed; it does not merge our list into the built-in catalogue or install anything by itself.
5. Choose your engines, permissions, and working folder in the app. No credentials or external accounts are provided by these templates.

## Individual files

Bloks can review a team Markdown file or a raw HTTPS Markdown link. A repository directory URL is not a team file. These team files use custom AORG skill IDs; a file import does not automatically read sibling skill folders. Use the AORG catalogue source for automatic resolution, or review/install the individual `SKILL.md` files separately and confirm their attachment to the correct agents. Do not assume a successful team preview proves all skills are attached.

For engineering, add Software Engineering and optionally the separate Engineering Review team. The former has seven builders/advisers; the latter has the two independent review roles. No multi-room legacy layout is recreated automatically.

## Check after adding

- Confirm the expected member count, role instructions, and exactly one most-senior lead.
- Confirm each member's referenced skills are present, attached, and reviewed. Inspect the installed app's actual enable/trust state; this repository makes no automatic-enablement claim.
- Set the intended working folder and per-agent approval levels. Prompt instructions are not an access-control mechanism.
- Do not enable schedules or external actions by default. This pack defines no routines.
- Try a harmless draft or read-only task before granting broader tools or access.

No live import, engine request, connected-app access, or cross-room handoff has been performed as part of creating this pack.
