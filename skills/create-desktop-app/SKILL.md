---
name: create-desktop-app
description: Create the executable PySide6 application foundation and standards-compliant Python package when the desktop phase selects PySide6.
---

# Create a PySide6 desktop application

Create `apps/desktop` with `pyproject.toml`, a `src/<package>/` package, `__main__.py`, GUI entry
point, resources, tests, README, and a `pysidedeploy.spec` or `[tool.pyside6.deploy]` configuration.
Use Qt Widgets unless requirements justify QML. Register `desktop` test commands for Ruff, mypy,
pytest/pytest-qt, `python -m build`, wheel inspection, and isolated `pipx` or virtual-environment
installation. Do not require a backend for local-only products.

Document terminal installation with `pipx install <wheel>` and, when the project has a public Git
remote, `pipx install git+https://...`. Also document the generated GUI command, upgrade, and
uninstall commands. Never execute an untrusted repository URL without validation and explicit user
intent.

Read [references/production-delivery.md](references/production-delivery.md) before writing the
foundation.
