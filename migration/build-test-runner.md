# Build Test Runner

In Exercism v3, one of the biggest changes is that we'll automatically check if a submitted solution passes all the tests.

We'll check this via a new, track-specific tool: the [_test runner_](https://github.com/exercism/v3-docs/tree/master/anatomy/track-tooling/test-runners). Each test runner is track-specific. When a new solution is submitted, we run the track's test-runner, which outputs a JSON file that describes the test results.

The test runner must be able to run the tests suites of both [Concept Exercises](https://github.com/exercism/v3-docs/blob/master/product/concept-exercises.md) and [Practice Exercises](https://github.com/exercism/v3-docs/blob/master/product/practice-exercises.md).

Each track must build a test runner according to [the spec](https://github.com/exercism/v3-docs/blob/master/anatomy/track-tooling/test-runners/interface.md). For tracks building a test runner from scratch, we have a [starting guide](https://github.com/exercism/v3-docs/blob/master/anatomy/track-tooling/test-runners/creating-from-scratch.md) and a [generic test runner](https://github.com/exercism/generic-test-runner/) that can be used as the base for the new test runner.

## Tracking

https://github.com/exercism/v3-launch/issues/4
