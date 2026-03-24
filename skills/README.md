# Skills

This directory is the central location for Claude Code skills used across all Codespaces.

## Structure

```
skills/
├── coding/      # Language-specific patterns, snippets, and conventions
├── git/         # Git workflow skills and commit conventions
└── shell/       # Shell scripting skills and utilities
```

## Adding Skills

Place skill files (Markdown `.md`, YAML `.yaml`, or plain text `.txt`) in the
appropriate sub-directory.  The installer copies the entire `skills/` tree to
`~/.claude/skills/` inside the Codespace.

### Example file layout

```
skills/coding/python-conventions.md
skills/git/conventional-commits.md
skills/shell/bash-best-practices.md
```

## Install / Update

Run the installer from the repo root:

```bash
bash bin/install-skills          # initial install
bash bin/install-skills --update # pull latest and re-sync
```

See `../README.md` for full instructions.
