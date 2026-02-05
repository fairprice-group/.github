# Contributing Guidelines

Thank you for your interest in contributing to FairPrice Group projects. This
document outlines the process and standards for contributing.

## Getting Started

1. Clone the repository
2. Create a new branch from `main` (or the repo's default branch)
3. Make your changes
4. Submit a pull request

## Branch Naming

Use the following conventions:

| Prefix | Purpose | Example |
|---|---|---|
| `feature/` | New features | `feature/add-cart-summary` |
| `fix/` | Bug fixes | `fix/checkout-total-calculation` |
| `chore/` | Maintenance tasks | `chore/update-dependencies` |
| `docs/` | Documentation only | `docs/update-api-guide` |
| `refactor/` | Code refactoring | `refactor/extract-payment-service` |

## Commit Messages

Follow [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(<scope>): <short summary>

<optional body>

<optional footer>
```

**Types:** `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`, `ci`, `perf`, `build`

Examples:
```
feat(cart): add quantity update endpoint
fix(auth): resolve token refresh race condition
docs(api): update authentication guide
```

### Commit Template

A `.gitmessage` template is available in this repository. To use it, configure Git
to load it automatically:

```bash
git config commit.template .gitmessage
```

This provides type prompts and formatting reminders each time you commit.

## Pull Request Process

1. **Keep PRs focused** -- one logical change per PR
2. **Fill out the PR template** completely
3. **Ensure CI passes** before requesting review
4. **Request review** from at least one code owner
5. **Address feedback** promptly and re-request review when ready
6. **Squash and merge** is the preferred merge strategy

## Code Review Expectations

**As an author:**
- Provide context in the PR description
- Self-review your diff before requesting others
- Respond to all comments, even if just to acknowledge

**As a reviewer:**
- Review within one business day where possible
- Be constructive and specific in feedback
- Approve when satisfied; don't block on nits

## Code Standards

- Follow the language-specific style guide for the project
- Write tests for new functionality
- Ensure existing tests pass
- Keep code DRY but don't over-abstract

## AI-Assisted Development

When using AI coding agents, follow the guidelines in [AGENTS.md](AGENTS.md).
Include a `Co-Authored-By` trailer in commits where AI assisted with the changes.

## Questions?

See [SUPPORT.md](SUPPORT.md) for how to get help, and
[CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) for community standards.
