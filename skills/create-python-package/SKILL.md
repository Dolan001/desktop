---
name: create-python-package
description: Create an installable Python library or CLI package without GUI requirements when the PRD selects a Python package deliverable.
---

# Create a Python package

Read the selected `Python package:` directive: `library`, `CLI`, or `both`. Create an independent
project under `packages/python/` with PEP 621 `pyproject.toml`, a `src/` package, tests, and a
README. Library mode exposes a documented importable API; CLI mode exposes `[project.scripts]` and
an argument-tested command; both mode provides both. Do not add PySide6, GUI entry points, tray
behavior, or native packaging unless another selected deliverable explicitly needs them.

Register package checks in `.ai/test-commands.json` under `desktop`: lint, typing, unit tests,
wheel and sdist build, and isolated install/import or CLI smoke tests. Document `pip install`
for libraries and `pipx install` for CLI tools. Preserve a separate `apps/desktop/` project when
the same PRD also selects a GUI app.
