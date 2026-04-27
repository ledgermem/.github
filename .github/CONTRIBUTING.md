# Contributing

Thanks for considering a contribution.

## Before you start

- For non-trivial changes, **open an issue first** to discuss approach.
- Read the target repo's `README.md` and `DECISIONS.md` if present.
- All commits must be **conventional commits** (`feat:`, `fix:`, `refactor:`, `docs:`, `test:`, `chore:`).

## Local dev

Each repo's README has a `## Development` section. The conventions are:

- **TypeScript repos**: `npm install && npm test && npm run build`
- **Python repos**: `pip install -e ".[dev]" && pytest && mypy src`

## Pull requests

1. Fork → branch from `main`
2. Make your change with tests
3. Run the full test suite locally — CI must be green
4. Open a PR using the template — fill out the test plan
5. One reviewer approval needed for merge

We squash-merge by default. Your PR title becomes the commit message — make it conventional.

## License

By contributing you agree your code is released under the repo's existing license (MIT for public repos unless otherwise noted).
