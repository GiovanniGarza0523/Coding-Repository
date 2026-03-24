# Coding-Repository

A centralized home for Giovanni's code, tools, and **Claude Code skills**.

---

## Claude Skills

The `skills/` directory contains reusable Claude Code skills following the
[Agent Skills standard](https://github.com/anthropics/skills). Each skill lives
in its own sub-folder with a `SKILL.md` file containing YAML frontmatter and
instructions that Claude loads dynamically.

Skills are automatically installed into every GitHub Codespace via the
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

1. Create a new directory under `skills/<category>/`.
2. Add a `SKILL.md` file with YAML frontmatter and instructions:
   ```markdown
   ---
   name: your-skill-name
   description: What this skill does and when Claude should use it.
   ---

   # Your Skill Title

   [Skill instructions here]
   ```
3. Commit and push.
4. Run `bash bin/install-skills --update` in any Codespace to get the latest.

### Skills structure

```
skills/
├── coding/
│   └── SKILL.md  - language conventions and patterns
├── git/
│   └── SKILL.md  - git workflow and commit conventions
└── shell/
    └── SKILL.md  - bash best practices and snippets
```

### SKILL.md format

Each `SKILL.md` follows the [Agent Skills specification](https://github.com/anthropics/skills):

| Frontmatter field | Required | Description                                      |
|-------------------|----------|--------------------------------------------------|
| `name`            | ✅        | Unique identifier for the skill (kebab-case)     |
| `description`     | ✅        | What the skill does and when Claude should use it|

### Automatic installation in Codespaces

Every new Codespace created from this repository will run
`bash bin/install-skills` automatically via `.devcontainer/devcontainer.json`.
