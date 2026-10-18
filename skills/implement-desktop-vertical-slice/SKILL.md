---
name: implement-desktop-vertical-slice
description: Implement a requirement-backed PySide6 desktop feature across domain, application, presentation, tests, and evidence.
---

# Implement a PySide6 vertical slice

Implement the smallest complete desktop behavior described by the task contract. Keep domain rules
independent of Qt, connect them through typed application services, and use signals for UI updates.
Test success, failure, cancellation, cleanup, keyboard use, and platform fallback. For animated
desktop companions, model animation state separately from movement and input; keep the window inside
available screen geometry and ensure users can always pause or exit.

Read [references/production-delivery.md](references/production-delivery.md) when the slice changes
packaging, process execution, resources, installation, or platform behavior.
