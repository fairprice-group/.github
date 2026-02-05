# .github

Organisation-wide default configurations for FairPrice Group GitHub repositories.

## What's Included

### Organisation Profile

- [`profile/README.md`](profile/README.md) -- displayed on the [FairPrice Group GitHub page](https://github.com/fairprice-group)

### Default Community Health Files

These apply to all repositories in the organisation that don't define their own:

| File | Description |
|---|---|
| [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md) | Code of conduct for contributors |
| [`CONTRIBUTING.md`](CONTRIBUTING.md) | Contributing guidelines, branching and commit conventions |
| [`SECURITY.md`](SECURITY.md) | Security vulnerability reporting process |
| [`SUPPORT.md`](SUPPORT.md) | Where to get help |

### Default PR Template

| File | Description |
|---|---|
| [`.github/PULL_REQUEST_TEMPLATE.md`](.github/PULL_REQUEST_TEMPLATE.md) | Default PR template with checklist |

### For AI Assistants

See [`AGENTS.md`](AGENTS.md) for behavioural guidelines when working in FairPrice
Group repositories.

### Developer Tooling

| File | Description |
|---|---|
| [`.gitmessage`](.gitmessage) | Commit message template following conventional commits |
| [`AGENTS.md`](AGENTS.md) | Org-wide AI coding agent behavioural guidelines |

## How It Works

GitHub automatically uses these files as defaults for all repositories in the
organisation. Any repository can override a default by creating its own version
of the file.

For example, if a repository has its own `CONTRIBUTING.md`, GitHub will use that
instead of the one here.

