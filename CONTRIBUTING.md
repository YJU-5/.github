# Contributing to Let Eat Go

Thank you for contributing to Let Eat Go.

## Workflow

1. Create or select a GitHub issue.
2. Create a branch from the latest `main`.
3. Keep the change focused on one purpose.
4. Run the relevant lint, test, and build commands.
5. Open a pull request and link the issue.
6. Address review feedback before merging.

Do not commit directly to `main`. It should remain stable and deployable.

## Branch Naming

Use lowercase English words and kebab-case:

```text
<type>/<short-description>
```

| Type | Purpose | Example |
| --- | --- | --- |
| `feature` | Add a feature | `feature/map-event-filter` |
| `bugfix` | Fix a non-critical bug | `bugfix/login-redirect-error` |
| `hotfix` | Fix an urgent production issue | `hotfix/oauth-token-validation` |
| `refactor` | Improve internal structure | `refactor/chat-service-structure` |
| `style` | Change visual styles or formatting | `style/profile-card-spacing` |
| `test` | Add or update tests | `test/album-api-coverage` |
| `docs` | Update documentation | `docs/backend-setup-guide` |
| `chore` | Update tooling or configuration | `chore/update-docker-config` |
| `experiment` | Explore an unreleased idea | `experiment/recommendation-model` |

## Commit Messages

Use a concise imperative subject:

```text
<type>: <summary>
```

Examples:

```text
feat: add Kakao Map event markers
fix: preserve authentication state after refresh
refactor: separate album API utilities
docs: add local setup instructions
```

Recommended types are `feat`, `fix`, `refactor`, `style`, `test`, `docs`, `chore`, and `perf`.

## Pull Requests

Include:

- What changed and why
- A link to the related issue
- Screenshots for visible UI changes
- Test steps and results
- Environment variable, migration, or deployment impact

Before requesting a review, inspect your own diff, remove debugging code, confirm that no secrets are included, and run the relevant checks.

## Secrets

- Never commit `.env`, API keys, tokens, passwords, or private credentials.
- Document variable names with safe placeholders in `.env.example`.
- Store deployment credentials in GitHub Actions secrets or use IAM roles.
- Revoke and rotate any credential that is accidentally committed.
