# TypeUI Cursor Plugin

TypeUI is a Cursor plugin that adds reusable commands to:

- install curated design `SKILL.md` files from `bergside/awesome-design-skills`
- generate or update local design-system skill files using `typeui.sh`
- list available curated skills with preview links

Browse curated design skills here: https://www.typeui.sh/design-skills

## Included commands

- `/typeui-list-skills`
- `/typeui-install-skill`
- `/typeui-generate-or-update`

## Requirements

- Node.js 18+
- `npx` available

## Install plugin locally in Cursor

1. Clone this repository.
2. Copy or symlink it into:
   - `~/.cursor/plugins/local/typeui/`
3. Restart Cursor (or reload window).
4. Open chat and type `/` to find the TypeUI commands.

## Command behavior summary

- Install command runs `pull` with a dry-run first, then applies changes.
- Generate/update command auto-selects `generate` vs `update` based on managed markers.
- Commands use non-interactive flags: `--format skill -p cursor`.

## Registry and CLI

- Registry: `https://github.com/bergside/awesome-design-skills`
- CLI: `https://github.com/bergside/typeui`

## License

MIT
