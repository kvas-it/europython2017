# Testing in Layers (A. Martelli)

Slides: http://www.aleax.it/europy17.pdf

- software system is a directed acyclic graph of dependencies (if you have
  cycles, fix that first),
- how do we test it:
  - ancient way: white-box, black-box
  - modern way (mostly the same stuff):
    - unit-test: white-boxy, dev-focused
    - integration tests: end-to-end
      - sometimes needs needs a human, but then it's QA and not automated
	testing
- best way: layers
  - unit test (fast, run all the time)
    - mock out dependencies,
    - fast (almost above all)
      - you can autorun them on save via IDE.
  - higher layer tests: match the code layers
    - you can see it as pattern language
- the fundamental things
  - all tests must be reproducible
    - if you have randomness, pin the seed
    - if depends on time, fake the time
  - test-driven approach to fixing bugs
- example: testing a DB adapter
  - in unit-tests: mock the DB (just an object with all the methods)
  - 2nd layer tests: fake - a dummy implementation that replicates the behavior
  - for full integration test: start and populate a real DB
  - if the DB, for example, fails when any method of connection is called after
    con.close()
    - fake must emulate this,
    - it would be good to program it into the mock as well, if you know it
- Mocks vs Fakes
  - https://martinfowler.com/articles/mocksArentStubs.html
  - a key issue: who owns/maintains it
    - A fake is usually maintained by the maintainers of the software itself,
      - sqlite has this
    - mock is very flexible, can simulate anything and lets you check calls
    - fake: fast limited emulation of real behavor of a specific component
- testing middle layer
  - mock out low layer components
  - in integration tests: use actual low layer components
    - if LL is fast enough, maybe you don't need unit tests but don't forget
      about simulating errors
- testing high layer
  - figure out the appropriate combination of mocking and using real ML and LL
    - mock -- fast but not quite accurate
    - fake -- fast and more accurate, but lots of work to build it
    - actual -- no extra work, but must be fast
- load testing in layers
  - actual ellapsed-time measurement needs the whole thing
  - but sometimes you can measure t + ∑n[i] \(where t is the time of your code
    and n[i] is the number of calls to external systems), and the you can
    calculate something useful
- testing & logging
  - unit-tests must be fast: check only what can be checked fast
  - for everything else, check logs in detail
  - batch sanity checks on logs/snaps: good idea, including production
