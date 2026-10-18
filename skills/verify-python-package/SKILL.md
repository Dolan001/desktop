---
name: verify-python-package
description: Independently verify Python library or CLI package behavior, wheel and sdist builds, and installation without requiring a GUI.
---

# Verify a Python package

Independently run the registered package checks. Build wheel and sdist, install the wheel in an
isolated environment, and verify the public import API for library mode, the installed command for
CLI mode, or both. Inspect packaged files and metadata. Record actual commands and outcomes in
desktop verification evidence. Do not substitute a GUI smoke test for package verification.
