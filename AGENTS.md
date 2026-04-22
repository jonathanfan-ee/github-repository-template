# AGENTS.md

> This file defines conventions for AI coding assistants (Claude Code, Cursor,
> Codex, Gemini CLI, Copilot, etc.) working in this repository.
> Human contributors should also read it.

## 0. Project Overview

<!-- TODO for new projects: replace {{}} placeholders -->

- **Name**: {{PROJECT_NAME}}
- **Purpose**: {{ONE-LINE WHAT/WHY}}
- **Status**: {{experimental | active | maintenance | archived}}
- **Maintainer**: Jonathan Fan ([@jonathanfan-ee](https://github.com/jonathanfan-ee))

## 1. Tech Stack

- **Language**: {{e.g., TypeScript / Python / Go}}
- **Framework**: {{e.g., Next.js / FastAPI / Gin}}
- **Runtime**: {{e.g., Node 20 / Python 3.12 / Go 1.22}}
- **Key deps**: {{3–5 critical libraries}}

## 2. How to Run

```bash
# Setup
{{install deps, e.g., pnpm install}}

# Development
{{start dev, e.g., pnpm dev}}

# Build
{{build, e.g., pnpm build}}

# Test
{{test, e.g., pnpm test}}
```

## 3. Architecture

```
src/
  ...
```

<!-- Brief description of key modules and what lives where. -->

## 4. Coding Conventions

- Follow project linter/formatter (eslint/prettier/ruff/gofmt/...).
- Match `.editorconfig` for indentation / EOL / charset.
- Name things clearly; prefer descriptive identifiers over comments.
- Only add comments when they explain *why*, not *what*.
- Avoid premature abstraction — rule of three (write it three times, then refactor).
- No speculative generality: don't add hooks/flags/options "in case we need them".

## 5. Git & Commit Conventions

- Default branch: `main`.
- Feature branches: `feat/<desc>`, `fix/<issue>`, `chore/<desc>`, `docs/<desc>`.
- Commit messages follow [Conventional Commits](https://www.conventionalcommits.org/).
  See `.github/COMMIT_CONVENTION.md` for type list.
- Prefer **new commits** over `--amend` when a hook fails.
- **Never** use `--no-verify` unless explicitly authorized.
- **Never** force-push to `main`.

## 6. Pull Request Flow

- Associate PRs with an Issue when possible.
- Keep PRs small and focused (< 400 lines diff preferred).
- Fill out `.github/PULL_REQUEST_TEMPLATE.md` — don't delete sections.
- Squash-merge by default (keeps `main` linear).

## 7. AI Tool Guidelines

> **Rules for AI agents editing this repo.**

### Do

- **Verify before claiming** — read current code, don't rely on memory/assumptions.
- **Grep before inventing** — confirm an API/function exists before using it.
- **Use task lists** for multi-step work (TodoWrite, etc.) so progress is trackable.
- **Test before reporting done** — at minimum run type checks and unit tests.
- **Match existing style** — don't introduce new patterns without discussion.

### Don't

- **Don't over-engineer** — solve the asked problem, not the hypothetical one.
- **Don't add unused code** — no speculative helpers, flags, or abstractions.
- **Don't commit `.env` or secrets** — verify `.gitignore` coverage before staging.
- **Don't `rm -rf` / force-push / skip hooks** without explicit user confirmation.
- **Don't narrate** — brief progress beats long monologues.

### Destructive operations

Before `rm -rf`, `git reset --hard`, `git push --force`, DB migrations, or
anything hard to reverse — **confirm with the user first**, even if the task
seems to imply it.

## 8. Secrets & Environment

- `.env` files are **never** committed. Use `.env.example` for the shape.
- Keys / certs / tokens live outside git (env vars, secret manager, or a
  file path outside the repo).
- If you spot a leaked secret in history, flag it immediately — don't quietly "fix" it.

## 9. Testing

- Unit tests: {{framework, e.g., vitest / pytest / go test}}
- Integration tests: {{framework or "manual for now"}}
- Run before commit: {{command}}

## 10. Communication Style (optional)

<!-- Personal preference — remove or adjust per project. -->

- The maintainer reads Chinese and English. Tool replies can be in either;
  default to whichever language the request was written in.
- Keep shell commands and code in English.

## 11. Contact

- Maintainer: Jonathan Fan (@jonathanfan-ee)
- GitHub Issues preferred for bugs / features.
- Security issues: {{email or security.md reference}}

---

<!--
Last reviewed: 2026-04-23

When updating:
1. Bump the "Last reviewed" date.
2. Ensure CLAUDE.md still does `@AGENTS.md`.
3. Mention changes in commit message with `docs(agents):` prefix.
-->
