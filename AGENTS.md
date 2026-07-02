# AGENTS.md

> **Project:** Teaching repository for *Working Critically with AI Coding Tools* workshop.
> **Core constraint:** Minimal changes only — do not fix, refactor, or improve anything unless explicitly asked.

## Toolchain

| Action | Command |
|---|---|
| Install deps | `pip install -r requirements.txt` |
| Permission model | `opencode.json` — destructive tools require confirmation |

## Judgment Boundaries

**NEVER**

- Fix, refactor, or improve code without an explicit request
- Make cosmetic or opportunistic changes beyond the minimal ask
- Commit secrets, tokens, or `.env` files
- Add dependencies without discussion

**ASK**

- Before running destructive operations (already gated by `opencode.json`)

**ALWAYS**

- Name the precise model (e.g., `deepseek-v4-flash-free`) in a `Co-Authored-By` trailer in every commit
- Use Conventional Commits format

## Commit Convention

```
<type>(<scope>): <imperative description>

<optional body — explain why, not what>

Co-Authored-By: <Model Name> <noreply@<provider>.com>
```

**Example:**

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
