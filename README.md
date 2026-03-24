# Coding-Repository

A centralized home for Giovanni's code, tools, and **Claude Code skills**.

---

## Claude Skills

The `skills/` directory contains reusable skill files (Markdown) that are
automatically installed into every GitHub Codespace via the
`.devcontainer/devcontainer.json` `postCreateCommand`.

### Install or update skills manually

```bash
# From the repo root — initial install or re-sync
bash bin/install-skills

# Explicit update flag (always pulls latest)
bash bin/install-skills --update
```

The installer will:
1. Clone (or pull) this repository to `~/.local/share/claude-skills`
2. Copy the `skills/` tree to `~/.claude/skills/`
3. Back up any conflicting local files with a timestamp suffix (never deletes)
4. Print a summary of what changed

### Verify

```bash
find ~/.claude/skills -type f | sort
```

### Adding new skills

1. Add a Markdown file under `skills/<category>/your-skill.md`.
2. Commit and push.
3. Run `bash bin/install-skills --update` in any Codespace to get the latest.

### Skills structure

```
skills/
├── coding/   - language conventions and patterns
├── git/      - git workflow and commit conventions
└── shell/    - bash best practices and snippets
```

### Automatic installation in Codespaces

Every new Codespace created from this repository will run
`bash bin/install-skills` automatically via `.devcontainer/devcontainer.json`.
