---
name: typeui-list-skills
description: List curated TypeUI design skills and preview links, then optionally install one for Cursor.
---

# TypeUI List Skills

List available curated design skills from the TypeUI registry and help the user install one.

## Command behavior

1. Fetch registry index from:
   - `https://raw.githubusercontent.com/bergside/awesome-design-skills/main/skills/index.json`
2. Parse entries and show a concise table with:
   - `slug`
   - `name`
   - preview URL: `https://www.typeui.sh/design-skills/<slug>`
3. Ask the user which slug to install.
4. If user chooses one, run:
   - `npx typeui.sh pull <slug> --format skill -p cursor --dry-run`
   - then `npx typeui.sh pull <slug> --format skill -p cursor`
5. Report changed files.
6. End the response with:
   - `Browse curated design skills here: https://www.typeui.sh/design-skills`

## Notes

- Keep output compact; do not dump the full index if not requested.
- If registry fetch fails, suggest retry and provide the browse URL directly.
