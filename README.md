# `.github`

Org-wide GitHub configuration for the [LedgerMem](https://github.com/ledgermem) organization.

This repo holds:

- **Reusable workflows** — `release.yml`, `node-test.yml`, `python-test.yml`, `docs-deploy.yml`, `publish-npm.yml`, `publish-pypi.yml`. Other repos consume these via `uses: ledgermem/.github/.github/workflows/<name>.yml@main`.
- **Org profile README** (`profile/README.md`) — what visitors see at https://github.com/ledgermem.
- **Issue / PR templates** — applied to every repo unless the repo overrides locally.
- **Dependabot config defaults**.

## Reusable workflows

| Workflow | Inputs | Purpose |
| --- | --- | --- |
| `node-test.yml` | `node-versions` (default `[20, 22]`), `working-directory` | `npm ci` + `tsc --noEmit` + `npm test` matrix |
| `python-test.yml` | `python-versions` (default `[3.10, 3.11, 3.12]`), `working-directory` | `pip install -e .[dev]` + `ruff` + `mypy` + `pytest` |
| `publish-npm.yml` | `package-path`, `tag` | Build + publish to npm with provenance, requires `NPM_TOKEN` org secret |
| `publish-pypi.yml` | `package-path` | Build + publish to PyPI with trusted publishing |
| `release.yml` | `release-script` (default `semantic-release`) | Conventional commits → tag → release |
| `docs-deploy.yml` | `working-directory` | Cloudflare Pages deploy |

Example consumer:

```yaml
# In any repo's .github/workflows/ci.yml
name: CI
on: [push, pull_request]
jobs:
  test:
    uses: ledgermem/.github/.github/workflows/node-test.yml@main
    with:
      node-versions: '[20, 22]'
```

## License

MIT — see [LICENSE](LICENSE).
