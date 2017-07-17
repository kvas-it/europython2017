# Faster Python: you have these choices (Paul Ross, MAN AHL)

## Intro and scope

- This is advice for general purpose computing,
- There's no free lunch. We're mostly looking at trade-offs.
- It's not about:
  - Numpy, Pandas,
  - Concurrency, caching.

- "Premature optimisation is the root of all evil in programming".

## Technology taxonomy

- What we would really want:
  - Can run Python code directly,
  - Works with all python version and 3rd party libraries,
  - Free,
  - Bug free,
  - Easy to debug,
  - 100x faster.
- In practice this doesn't exist and we'll be making trade-offs.

- No code change:
  - Cython without annotations (x1.3 without changes),
  - Pypy (x7 but compatibility),
  - Shedskin (unmaintained),
  - Pyston (suspended :( ).

- Some code change:
  - Cython optimised (x62 on the example, but hard to maintain),
  - Numba (compatible, backed by Continuum, easy changes),
  - Parakeet (unmaintained),
  - Pythran (annotation, generate C++, not so active).

- Other language (x100+):
  - CPython C extension (lots of work, hard to test),
  - ctypes,
  - CFFI (quite a bit easier than C API),
  - PyBind11 (C++11, pretty easy),
- Try to isolate your C code from Python code, that makes testing easier.

## Evaluation criteria

- Who you are
  - What constraints your culture imposes on you?
  - What skills do you have and can acquire (or might lose)?

- Technical criteria
  - Dependencies,
  - Supported python versions,
  - Compatibility,
  - Benchmarks: although all benchmarks are wrong because benchmarking is hard
    to make representative.

- Non-technical criteria
  - Ease of installation and deployment,
  - Dependencies,
  - Ease of writing code,
  - Ease of maintenance,
  - Ease of debugging,
  - Development status:
    - Age,
    - Maintained?
    - Company backers?
    - Large community?
    - Fixes are quick?
    - PRs accepted?

## Other notes

- https://www.python.org/dev/peps/pep-0523/
- High Performance Python book.
