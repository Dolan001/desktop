# Architecture

Keep the Qt event loop responsive. Use signals, timers, worker objects, or `QProcess` for asynchronous
work. Represent movement and animation as testable state, not timer callback side effects. Use
`QSettings` or a documented local store for non-secret preferences and the OS credential store for
credentials.
