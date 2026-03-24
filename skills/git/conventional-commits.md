# Git Skills

## Commit Conventions (Conventional Commits)

Format: `<type>(<scope>): <short summary>`

| Type       | When to use                                  |
|------------|----------------------------------------------|
| `feat`     | A new feature                                |
| `fix`      | A bug fix                                    |
| `docs`     | Documentation only changes                   |
| `style`    | Formatting, missing semicolons, etc.         |
| `refactor` | Code change that is neither fix nor feature  |
| `test`     | Adding or correcting tests                   |
| `chore`    | Build process or tooling changes             |

## Branching

- `main` — stable, always deployable
- `feature/<name>` — new work
- `fix/<name>` — bug fixes

## Workflow

1. Branch off `main`.
2. Commit often with descriptive messages.
3. Open a PR and request review before merging.
