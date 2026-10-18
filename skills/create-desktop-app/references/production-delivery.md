# Production delivery

Use a `src` layout and `[project.gui-scripts]`. Package icons, sprites, translations, and licenses;
test their lookup from an installed wheel rather than the source checkout. Keep UI callbacks small,
route failures to visible recoverable states, and never block the event loop with subprocess or
network work. Security checks must cover argument-array process launching and untrusted repository
URLs. Verification must build both wheel and sdist, install the wheel in isolation, launch a bounded
smoke mode, and report errors truthfully. Native delivery uses `pyside6-deploy` on each target OS;
signing credentials remain outside source control.
