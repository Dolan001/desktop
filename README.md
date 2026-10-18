# Python Desktop workflow pack

Behavior-only guidance for generating, testing, packaging, and independently verifying Python
desktop applications and standalone no-GUI packages. It contains no finished application.

## Choose deliverables in the PRD

| Directive | Generated project | What users get |
|---|---|---|
| `Desktop framework: Python Desktop` | `apps/desktop/` | PySide6 GUI app |
| `Python package: library` | `packages/python/` | Importable Python API |
| `Python package: CLI` | `packages/python/` | Installed command |
| `Python package: both` | `packages/python/` | Importable API and installed command |

The GUI and package directives may appear together. `$start-build` then builds both; `$start-desktop`
stops after their shared verification gate. From a target project with a PRD, the CLI equivalent is
`./.agents/bin/ai start-desktop --project . --github-user <your-github-user>`. The PRD already
provides the selection, so separate framework flags are optional.

A generated desktop application is also an installable Python package. Its Python source,
resources, tests, `pyproject.toml`, and GUI entry point live together under `apps/desktop/` in the
target project. Users can install its wheel with `pipx` or `pip`; native OS bundles are additional
release artifacts built from the same application source. This behavior pack contains instructions
for producing both forms, not a copy of a finished application.

The same behavior pack can also produce a standalone Python library, a command-line package, or
both under `packages/python/`. Those deliverables have no GUI requirement. A PRD may select both
the PySide6 app and the standalone package; they remain independently buildable and installable.

## What verification checks

Each selected project needs a wheel, sdist, and isolated-install smoke test. GUI verification also
covers the launcher, behavior, accessibility, and truthful native packaging readiness. Package
verification covers its public import API, installed command, or both, without requiring Qt.
Evidence and checkpoints live in the target project's `.ai/` directory. A local-only GUI or
package does not require a backend unless the PRD calls for one.

`agents/` defines implementer and verifier roles; `skills/` separates GUI and standalone-package
guidance; `rules/` contains both structure contracts; `hooks/` and `commands/` constrain work.
