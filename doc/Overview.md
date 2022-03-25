# Code Lines: Overview

A code line is denoted by a naming pattern for the semantic versioning
sequence within it.

For example, consider `0.1.x-alpha.2.y`.  Here `x` and `y` indicate
variables; pieces of the semantic version that are allowed to increase
monotonically.  The patch level `x` normally starts at 0, and increases
monotonically (if at all), within the code line.  The sequence number `y`
normally starts at 1, and increases monotonically for each official build
that occurs against a commit within the code line.

All other parts of a code line's semantic versioning pattern are fixed.
Incrementing one of those parts 'promotes' the code line, and
conversely, decrementing one of those parts 'demotes' the code line.

A code line is promoted as the code base evolves and improves.  For
example, the behavior contract might evolve through 0.0, 0.1, on up
to 1.0 and beyond.  And the development phase might evolve through
alpha.0, alpha.1, alpha.2, beta.0, beta.1, rc.0, rc.1, and so on.

Note that the development phase resets whenever the major version of the
behavior contract changes.  And the sequence number resets whenever the
development phase resets.  For example:
```
    0.0.0-alpha.0.1  0.0.0-alpha.0.2  ...

    0.0.0-alpha.1.1  0.0.0-alpha.1.2  ...

    0.1.0-beta.1.1   0.1.0-beta.1.2   ...

    0.2.0-rc.1.1     0.2.0-rc.1.2     ...

    0.2.0                             ...

    0.2.1                             ...

    1.0.0-alpha.0.1  1.0.0-alpha.0.2  ...

    1.0.0-alpha.1.1  1.0.0-alpha.1.2  ...
```

Details about semantic versioning can be found [here](<https://semver.org>).
