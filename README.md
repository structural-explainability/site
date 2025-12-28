# Site: Structural Explainability

[![License: Apache-2.0](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](./LICENSE)
[![Deploy Docs](https://github.com/structural-explainability/site/actions/workflows/deploy-docs.yml/badge.svg?branch=main)](https://github.com/structural-explainability/site/actions/workflows/deploy-docs.yml)
[![Dependabot](https://img.shields.io/badge/Dependabot-enabled-brightgreen.svg)](https://github.com/structural-explainability/site/security/dependabot)

> Documentation site for Structural Explainability.

This repository hosts the public-facing site built with MkDocs and deployed
via GitHub Pages. It is docs-only and does not produce a Python package.

## Install

- uv
- VS Code (recommended)

## One-Time Setup

Create a local environment and install dependencies.

```shell
uv self update
uv python pin 3.12
uv venv

# Windows:
.venv\Scripts\activate

# macOS/Linux:
# source .venv/bin/activate

uv sync --extra dev --extra docs --upgrade
uvx pre-commit install
```

## Local Checks (Pre-commit)

```shell
git add .
uvx pre-commit autoupdate
uvx pre-commit run --all-files
```

## Build and Serve Docs

```shell
uv run mkdocs build --strict
uv run mkdocs serve
```

## Annotations

[Annotations.md](./ANNOTATIONS.md)

## License

[MIT](./LICENSE)
