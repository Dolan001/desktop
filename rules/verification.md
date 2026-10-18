# Verification

Verify installed-package behavior, not only source-tree imports. For standalone libraries, test
public imports; for CLI packages, test installed commands and exit codes. Run Qt UI tests only when
a GUI is selected. Preserve truthful platform-specific checks for always-on-top, system tray,
signing, and Wayland behavior, and report unsupported environments as limitations.
