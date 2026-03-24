# Shell Skills

## Bash Best Practices

- Always start scripts with `#!/usr/bin/env bash` and `set -euo pipefail`.
- Quote variables: `"$var"` not `$var`.
- Use `[[ … ]]` for conditionals instead of `[ … ]`.
- Prefer `$()` over backticks for command substitution.
- Use `local` for all variables inside functions.
- Provide a `--help` flag in every CLI script.

## Useful Patterns

```bash
# Safe directory creation
mkdir -p "${target_dir}"

# Timestamped backup before overwriting
cp -a "${file}" "${file}.bak.$(date +%Y%m%d%H%M%S)"

# Check if a command exists
if ! command -v git &>/dev/null; then
  echo "git is not installed" >&2
  exit 1
fi
```
