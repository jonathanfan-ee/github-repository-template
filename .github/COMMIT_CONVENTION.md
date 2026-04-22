# Commit Message Convention

This project follows [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)
for commit messages. This enables readable history and automated changelog generation.

## Format

```
<type>(<scope>): <subject>

<body>

<footer>
```

- **type** and **subject** are required
- **scope** is optional (area of the code affected)
- Subject < 72 chars, imperative mood ("add" not "added")

## Types

| Type | When |
|---|---|
| `feat` | New feature for the user |
| `fix` | Bug fix for the user |
| `docs` | Documentation only |
| `style` | Formatting / whitespace, no code change |
| `refactor` | Code change that neither fixes nor adds |
| `perf` | Performance improvement |
| `test` | Adding or fixing tests |
| `build` | Build system or dependencies |
| `ci` | CI configuration changes |
| `chore` | Housekeeping, tooling |
| `revert` | Reverts a previous commit |

## Breaking changes

Add `!` after type or `BREAKING CHANGE:` in footer:

```
feat(api)!: drop support for Node 16
```

## Examples

```
feat(auth): add OAuth2 Google provider
fix(ui): correct button alignment on mobile
docs: update installation steps
chore(deps): bump react from 18.2 to 18.3
refactor(api): extract user validation into middleware
```

## Revert

When reverting a commit, use:

```
revert: <original commit header>

This reverts commit <hash>.
```

## References

- [Conventional Commits v1.0](https://www.conventionalcommits.org/en/v1.0.0/)
- [commitlint](https://commitlint.js.org/) — lint messages automatically
- [commitizen](https://github.com/commitizen/cz-cli) — interactive wizard
