# Contributing

Thanks for your interest in contributing! This document explains how to report
issues, propose changes, and submit pull requests.

## Reporting issues

- Use [GitHub Issues](../../issues) with the appropriate template
  (`bug_report` or `feature_request`).
- For bugs, include reproduction steps, expected vs. actual behavior, and
  environment info (OS, runtime version).
- For security issues, do **not** open a public issue. Contact the maintainer
  privately at **jofanexus@gmail.com**.

## Proposing changes

1. For non-trivial changes, **open an issue first** to discuss scope.
2. Fork the repository and create a feature branch:
   - `feat/<short-desc>` for features
   - `fix/<issue-number>` for bug fixes
   - `docs/<short-desc>` for documentation
   - `chore/<short-desc>` for tooling / refactors
3. Make your changes. Follow the conventions in [AGENTS.md](AGENTS.md).
4. Run tests and linters locally before pushing.
5. Open a Pull Request against `main` using the PR template.

## Commit messages

Follow [Conventional Commits](https://www.conventionalcommits.org/) — see
[.github/COMMIT_CONVENTION.md](.github/COMMIT_CONVENTION.md) for the type list.

## Code style

- Match the project's formatter/linter (check `package.json`, `pyproject.toml`,
  or language-specific configs).
- Respect `.editorconfig` for indentation / line endings / charset.
- Keep PRs focused and small (< 400 lines diff preferred).

## Review & merge

- PRs are squash-merged by default.
- The maintainer may request changes before merging.
- Be patient — this is a personal project; responses may take a few days.
