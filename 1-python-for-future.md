# Python for the Future Generations (A. Ronacher)

- python is whatever cpython does, there's no standard
- all other implementations have to copy the quirks
- example: a + b is complicated in python
- backwards compatibility is valued in python community...
- also in packaging...
- and the GIL
- one exception was python3 - both too radical and also not radical enough

## What we do good
- interpreter code is readable,
- dependency hierarchies are flat,
- runtime introspection is good.

## Improve
- packaging
  - package.json, Cargo.toml -- package metadata
    - no code run on install
    - packages can introspect their own version and dependencies.
  - where are we now
    - mostly people use pip instead of setup.py install,
      - we could get away from setup.py
- language standard
  - but nobody would want to make current implementation the standard,
  - maybe micropython could lead the way,
  - kill extension API for CFFI -- fix the docs!
- unicode
  - rust string internal encoding:
    - utf-8 everywhere
    - wtf-8 where it doesn't work
  - python has dynamically upgrading strings: 1 byte per char -> 2 bpc -> 4 bpc
  - we should probably go to using utf-8 instead
    - we'll lose string slicing and constant time character access but that's
      ok
- only use CFFI
  - hard for things like numpy
  - generally possible for most others
- linters and type annotations:
  - babel
  - typescript, flow
  - one true formatting

## What can we do personally
- Abuse the language less
