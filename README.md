# Site: Structural Explainability

[![License: Apache-2.0](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](./LICENSE)
[![Deploy Docs](https://github.com/structural-explainability/site/actions/workflows/deploy-docs.yml/badge.svg?branch=main)](https://github.com/structural-explainability/site/actions/workflows/deploy-docs.yml)
![Build Status](https://github.com/structural-explainability/site/actions/workflows/ci-hygiene-mkdocs.yml/badge.svg?branch=main)
[![Check Links](https://github.com/structural-explainability/site/actions/workflows/links.yml/badge.svg)](https://github.com/structural-explainability/site/actions/workflows/links.yml)
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
uv sync --extra dev --extra docs --upgrade

uvx pre-commit install
git add -A
uvx pre-commit run --all-files
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
