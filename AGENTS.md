# Python desktop and package behavior pack

This pack contains instructions and contracts only. Generate a selected GUI app under the target
project's `apps/desktop/` and a selected standalone library or CLI under `packages/python/`.
Do not require Qt in a package-only project. For a GUI, prefer Qt Widgets unless requirements
justify QML, and provide an explicit exit action for frameless companions. Build each selected
deliverable as an independently installable Python project.
