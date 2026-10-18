---
name: package-desktop-app
description: Build and validate wheel, sdist, pipx installation, and PySide6 native packaging outputs for a desktop release.
---

# Package a PySide6 desktop application

Build the wheel and sdist with `python -m build`, validate metadata, install the wheel into an
isolated environment, and launch its GUI entry point in bounded smoke mode. Configure
`pyside6-deploy` for standalone native output. Treat macOS, Windows, and Linux builds as separate
platform jobs; never claim cross-platform success from one host. Generate checksums and keep code
signing or notarization credentials in the release environment only. Verify the documented
`pipx install <wheel>` command. If a public Git remote is part of the delivery contract, also verify
the exact `pipx install git+https://...` form in an isolated environment without weakening URL or
revision validation.
