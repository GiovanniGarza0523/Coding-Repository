---
name: coding-conventions
description: Language conventions and patterns for Python, JavaScript/TypeScript, and general coding best practices. Use this skill when writing or reviewing code to ensure consistent style, type safety, and clean design.
---

# Coding Skills

## Python

- Use type hints for all function signatures.
- Prefer `pathlib.Path` over `os.path`.
- Use `dataclasses` or `pydantic` for structured data.
- Write docstrings in Google style.

## JavaScript / TypeScript

- Prefer `const` over `let`; avoid `var`.
- Use `async/await` instead of raw Promise chains.
- Keep functions small (≤ 30 lines where possible).

## General

- Follow the existing style of the file you are editing.
- One responsibility per function.
- Prefer explicit over implicit.
