# Template Usage

This document describes the `github-repository-template` structure and how to
use it. **If you created your own repo from this template, you can safely
delete this file (and the `docs/` directory if empty).**

## What this template is

A minimal starting point for a new GitHub repository. It covers the usual
hygiene files (LICENSE, .gitignore, .editorconfig, .gitattributes), modern
AI-tooling conventions (AGENTS.md, CLAUDE.md), and GitHub-flavored templates
(PR template, Issue templates).

## How to use

1. On the template repo on GitHub, click **Use this template → Create a new
   repository**.
2. Clone your new repo locally.
3. Fill in `{{PROJECT_NAME}}`, `{{ONE-LINE DESCRIPTION}}`, and other `{{}}`
   placeholders in:
   - `README.md`
   - `README.en-US.md`
   - `AGENTS.md`
4. Delete files you don't need:
   - `docs/TEMPLATE_USAGE.md` (this file) — after reading
   - `CODE_OF_CONDUCT.md` — if it's not a public/open-source project
   - `CONTRIBUTING.md` — if it's a solo/internal project
   - `README.en-US.md` — if you don't need English
5. Run the first commit:
   ```bash
   git add -A
   git commit -m "chore: init from template"
   ```

## File index

| File | Purpose |
|---|---|
| `LICENSE` | Apache 2.0 — replace copyright holder if forking |
| `README.md` / `README.en-US.md` | Project overview (bilingual) |
| `AGENTS.md` | AI-agent + team coding conventions (Cursor / Claude / Codex / Gemini read this) |
| `CLAUDE.md` | Claude Code entry point (imports AGENTS.md) |
| `.gitignore` | Node / Go / Python / Unity / AI tool configs / OS junk |
| `.gitattributes` | Line-endings, binary tagging, GitHub language stats |
| `.editorconfig` | Cross-editor indent / charset / EOL |
| `.github/PULL_REQUEST_TEMPLATE.md` | PR checklist |
| `.github/ISSUE_TEMPLATE/bug_report.md` | Bug report template |
| `.github/ISSUE_TEMPLATE/feature_request.md` | Feature request template |
| `.github/ISSUE_TEMPLATE/config.yml` | Disables blank issues |
| `.github/COMMIT_CONVENTION.md` | Conventional Commits reference |
| `CHANGELOG.md` | Keep a Changelog format |
| `CONTRIBUTING.md` | How to contribute |
| `CODE_OF_CONDUCT.md` | Contributor Covenant 2.1 |

## Template maintainer

[@jonathanfan-ee](https://github.com/jonathanfan-ee)
