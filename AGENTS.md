# AGENTS.md — Instructions for AI Coding Agents

## Purpose

This is a **teaching repository** for the *Working Critically with AI Coding Tools* workshop. Do not fix, refactor, or improve anything unless explicitly asked. When asked, only make the minimal change requested — resist the urge to clean up unrelated issues.

## AI Use Policy

AI assistance is **expected and encouraged**. However, the commit message body **must name the precise model** used (e.g., `deepseek-v4-flash-free`, `claude-sonnet-4-20250514`, `gpt-4o-2025-01-20`, etc.) in a `Co-Authored-By` trailer.

## Example Commit Message (Conventional Commits)

```
feat(agents): Add AGENTS.md with project conventions

Explain the repo is a teaching environment and agents should
not make unsolicited fixes. Document the AI use policy
requiring precise model attribution in commit messages.

Co-Authored-By: deepseek-v4-flash-free <noreply@deepseek.com>
```

- **Type**: `feat`, `fix`, `docs`, `refactor`, `chore`, etc.
- **Scope** (optional): `(agents)`, `(devcontainer)`, `(notebook)`, etc.
- **Description**: Imperative, present tense, no trailing period.
- **Body** (optional): Brief explanation of *why*.
- **Trailer**: `Co-Authored-By: <Model Name> <noreply@<provider>.com>`
