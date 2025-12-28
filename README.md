# Site: Structural Explainability

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
