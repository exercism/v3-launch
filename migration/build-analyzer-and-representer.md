# Build Representer and Analyzer

## Representer

In Exercism v3, we're introducing a new (optional) tool: the [representer](https://github.com/exercism/v3-docs/tree/master/anatomy/track-tooling/representers). The goal of the representer is to take a solution and returning a representation, which is an extraction of a solution to its essence with normalized names, comments, spacing, etc. but still uniquely identifying the approach taken. Two different ways of solving the same exercise must not have the same representation.

Each representer is track-specific. When a new solution is submitted, we run the track's representer, which outputs two JSON files that describe the representation.

Once we have a normalized representation for a solution, a team of vetted mentors will look at the solution and comment on it (if needed). These comments will then automatically be submitted to each new solution with the same representation. A notification will be sent for old solutions with a matching representation.

Each track should build a representer according to [the spec](https://github.com/exercism/v3-docs/blob/master/anatomy/track-tooling/representers/interface.md). For tracks building a representer from scratch, we have a [starting guide](https://github.com/exercism/v3-docs/blob/master/anatomy/track-tooling/representers/creating-from-scratch.md).

The representer is an optional tool though, which means that if a track does not have a representer, it will still function normally.

## Analyzer

In Exercism v3, we are making increased use of our v2 [analyzers](https://github.com/exercism/v3-docs/tree/master/anatomy/track-tooling/analyzers). Analyzers automatically assess student's submissions and provide mentor-style commentary. They can be used to catch common mistakes and/or do complex solution analysis that can't easily be done directly in a test suite.

Each analyzer is track-specific. When a new solution is submitted, we run the track's analyzer, which outputs a JSON file that contains the analysis results.

In v2, analyzer comments were given to a mentor to pass to a student. In v3, the analyzers will normally output directly to students, although we have added an extra key to output suggestions to mentors. If your track already has an analyzer, the only requisite change is updating the outputted copy to be student-facing.

Each track should build an analyzer according to [the spec](https://github.com/exercism/v3-docs/blob/master/anatomy/track-tooling/analyzers/interface.md). For tracks building an analyzer from scratch, we have a [starting guide](https://github.com/exercism/v3-docs/blob/master/anatomy/track-tooling/analyzers/creating-from-scratch.md).

The analyzer is an optional tool though, which means that if a track does not have an analyzer, it will still function normally.

## Choosing between representer and analyzer

If you want to build both, our recommendation is to start building the representer first for the following reasons:

- Representers are usually (far) easier to implement
- Representers can have a far bigger impact on the mentoring load than analyzers by empowering mentors
- Representers apply to _all_ exercises, whereas analyzers usually target specific exercises or a subset

## Tracking

https://github.com/exercism/v3-launch/issues/8
