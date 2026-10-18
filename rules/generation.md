# Generation

Generate only inside leased target paths. Provide a `--smoke-test` or equivalent bounded launch mode
for CI. Include resources in the package and register deterministic commands in
`.ai/test-commands.json`. Never add platform signing material.
The generated README must include terminal install, launch, upgrade, and uninstall commands for the
Python package, plus native installer instructions only for bundles actually produced and tested.
