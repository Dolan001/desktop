---
name: implement-python-package-vertical-slice
description: Implement requirement-backed behavior in a standalone Python library or CLI package selected by the PRD.
---

# Implement a Python package slice

Implement the selected library API and/or CLI command under `packages/python/`. Keep imports free
of GUI initialization. Test public API behavior, command arguments and exit codes where applicable,
errors, and installed-wheel behavior. If the desktop GUI also uses this package, declare the
dependency and verify the integration without copying package source into the app.
