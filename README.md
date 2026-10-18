# Python Desktop workflow pack

Behavior-only guidance for generating, testing, packaging, and independently verifying PySide6
desktop applications.

A generated desktop application is also an installable Python package. Its Python source,
resources, tests, `pyproject.toml`, and GUI entry point live together under `apps/desktop/` in the
target project. Users can install its wheel with `pipx` or `pip`; native OS bundles are additional
release artifacts built from the same application source. This behavior pack contains instructions
for producing both forms, not a copy of a finished application.
