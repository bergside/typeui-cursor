---
name: typeui-install-skill
description: Install a curated TypeUI design SKILL.md locally for Cursor from the awesome-design-skills registry.
---

# TypeUI Install Skill

Install one curated design skill from `bergside/awesome-design-skills` into this project for Cursor.

## Command behavior

1. Parse the requested slug from the user's message.
2. If slug is missing:
   - Fetch `https://raw.githubusercontent.com/bergside/awesome-design-skills/main/skills/index.json`
   - Show a concise list of available slugs and ask which one to install.
3. Validate slug format: lowercase letters, numbers, dashes, or underscores.
4. Run a preview first:
   - `npx typeui.sh pull <slug> --format skill -p cursor --dry-run`
5. If preview looks correct, run the real install:
   - `npx typeui.sh pull <slug> --format skill -p cursor`
6. Report created/updated files and whether they changed.
7. Mention that TypeUI currently also writes the universal skill file:
   - `.agents/skills/design-system/SKILL.md`
8. End the response with:
   - `Browse curated design skills here: https://www.typeui.sh/design-skills`

## Notes

- Prefer deterministic flags (`--format skill -p cursor`) to avoid interactive prompts.
- If `typeui.sh` is unavailable, guide the user to run `npx typeui.sh --help` and retry.
