---
name: write-tests
description: Writes unit tests for a function, module or change, following
  the project's existing test framework and patterns. Use when the user asks
  for tests, more test coverage, or to test a function or bug fix.
---

# Write tests

1. Find the existing tests closest to the code under test. Copy their
   framework, file naming, folder layout and helper usage.
2. List the behaviors to cover before writing code:
   - The main success path
   - Edge cases: empty, zero, null, very large, unicode
   - Error paths: invalid input, failed dependencies
   - The exact bug, if this is a bug fix (the test must fail without the fix)
3. One behavior per test. Name tests after the behavior:
   "returns zero for an empty cart".
4. Mock only what crosses a boundary: network, clock, randomness,
   filesystem. Don't mock the code under test.
5. Run the tests. Fix failures caused by the tests themselves. If a test
   reveals a real bug, stop and report it instead of changing the code.

If no test framework is set up, ask before adding one.
