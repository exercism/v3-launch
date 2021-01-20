# Build Test Runner

In Exercism V3, one of the biggest changes is that we'll automatically check if a submitted solution passes all the tests.

We'll check this via a new, track-specific tool: the [_test runner_](https://github.com/exercism/v3-docs/tree/master/anatomy/track-tooling/test-runners). The test runner is track-specific and implemented as a Docker image. Whenever a solution is submitted, a Docker container is created of that image and it runs on the submitted solution. The test runner outputs a JSON file that describes the test results.

Each track must build a test runner according to [the spec](https://github.com/exercism/v3-docs/blob/master/anatomy/track-tooling/test-runners/interface.md).

## Tracking

https://github.com/exercism/v3-launch/issues/4
