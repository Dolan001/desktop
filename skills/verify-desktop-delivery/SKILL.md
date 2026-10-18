---
name: verify-desktop-delivery
description: Independently verify an implemented PySide6 app and its Python-package and native-release evidence.
---

# Verify PySide6 delivery

Run registered commands from the target repository without a shell. Require passing lint, typing,
unit, UI, package build, isolated installation, and launch smoke checks. Verify resource loading from
the installed artifact and confirm uninstall leaves no application files outside documented user
settings. Validate native bundles only on platforms where they were built and exercised. Write
`verified: true` only when all applicable checks pass and no critical blocker remains.
