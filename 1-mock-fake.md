# But how do you know your mock is valid? (Adam Dangoor)

- Testing with real remote services has problems:
  - Network is not stable, 3rd party services also break,
  - Some services cost money and/or have resource limits,
  - The tests become slow.
- So you can mock stuff, but if the mocks get elaborate:
  - You don't get them right,
  - They get out of date (and finding that automatically is not trivial),
  - So you can start building the mocks in a more structured way
- Make a separate mock using Flask
  - Can be used with any test framework
  - Can even be run as a standalone process
  - You're replicating some of the work of the service programmers...
- At this point you want a a verified Fake
  - Which means that it was tested by parts of the same test suite,
  - Since we don't have the tests of the real code, we can just write
    characteristic tests for the web service and then also run them against the
    fake.
  - We can run the tests and see that our mock/fake still matches the real
    thing.
- So if you're shipping software that other people will use and depend on and
  that they will want to call in test, shipping a verified fake with it would
  be very valueable (and it's much easier for you than for third party
  developers given that you have the original source code and its test suite).

## From QA

- The mock should be able to simulate errors (via some kind of introspection
  API).
- When you need to test context-specific conditions, you can use the backend
  API of the fake to set the conditions. To verify this, you can have a test
  account with the service that has those conditions manually precreated.
- Idea: test against real service but cache the responses, then the tests just
  run against the cache (VCR system).
