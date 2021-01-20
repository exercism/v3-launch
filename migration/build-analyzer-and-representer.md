# Build Analyzer and Representer

## Representer

In Exercism v3, we're introducing a new (optional) tool: the [_representer_](https://github.com/exercism/v3-docs/tree/master/anatomy/track-tooling/representers). The goal of the representer is to take a solution and returning a representation, which is an extraction of a solution to its essence with normalized names, comments, spacing, etc. but still uniquely identifying the approach taken. Two different ways of solving the same exercise must not have the same representation.

Once we have a normalized representation for a solution, a team of vetted mentors will look at the solution and comment on it (if needed). These comments will then automatically be submitted to each new solution with the same representation. A notification will be sent for old solutions with a matching representation.

Whenever a solution is submitted, a Docker container is created of the representer image and it runs on the submitted solution. The test runner outputs two JSON files that describe the representation. See [the spec](https://github.com/exercism/v3-docs/blob/master/anatomy/track-tooling/representers/interface.md).

The representer is an optional tool, which means that if a track does not have a representer, it will still function normally.

## Analyzer

In Exercism v3, we are making increased use of our v2 [analyzers](https://github.com/exercism/v3-docs/tree/master/anatomy/track-tooling/analyzers). Analyzers automatically assess student's submissions and provide mentor-style commentary. They can be used to catch common mistakes and/or do complex solution analysis that can't easily be done directly in a test suite.

In v2, analyzer comments were given to a mentor to pass to a student. In v3, the analyzers will normally output directly to students, although we have added an extra key to output suggestions to mentors. If your track already has an analyzer, the only requisite change is updating the outputted copy to be student-facing.

Whenever a solution is submitted, a Docker container is created of the analyzer image and it runs on the submitted solution. The analyzer outputs a JSON file that contains the analysis results. See [the spec](https://github.com/exercism/v3-docs/blob/master/anatomy/track-tooling/analyzers/interface.md).

The analyzer is an optional tool, which means that if a track does not have an analyzer, it will still function normally.

## Choosing between representer and analyzer

If you want to build both, our recommendation is to start building the representer first for the following reasons:

- Representers are usually (far) easier to implement
- Representers can have a far bigger impact on the mentoring load than analyzers by empowering mentors
- Representers apply to _all_ exercises, whereas analyzers usually target specific exercises or a subset

## Tracking

https://github.com/exercism/v3-launch/issues/8
