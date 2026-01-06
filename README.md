# Site: Structural Explainability

[![License: Apache-2.0](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](./LICENSE)
[![Deploy Docs](https://github.com/structural-explainability/site/actions/workflows/deploy-docs.yml/badge.svg?branch=main)](https://github.com/structural-explainability/site/actions/workflows/deploy-docs.yml)
[![Dependabot](https://img.shields.io/badge/Dependabot-enabled-brightgreen.svg)](https://github.com/structural-explainability/site/security/dependabot)

> Documentation site for Structural Explainability.

This repository hosts the public-facing site built with MkDocs and deployed
via GitHub Pages. It is docs-only and does not produce a Python package.

## Developer

Steps to run pre-commit locally. Install `uv`.

Initialize once:

```shell
uv self update
uv python pin 3.12
uvx pre-commit install
uvx pre-commit run --all-files

# Windows:
.venv\Scripts\activate

# macOS/Linux:
# source .venv/bin/activate

uv sync --extra dev --extra docs --upgrade
```

Build and serve docs:

```shell
uv run mkdocs build --strict
uv run mkdocs serve
```

Save progress as needed:

```shell
git add -A
# If pre-commit makes changes, re-run `git add -A` before committing.
git commit -m "update"
git push -u origin main
```


## Annotations

[Annotations.md](./ANNOTATIONS.md)

## License

[MIT](./LICENSE)
