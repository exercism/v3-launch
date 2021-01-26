# Update status

There are several new features in Exercism v3 for tracks to build. To selectively enable these features on the Exercism v3 website, each track must keep track of the status of the following features:

- [Concept Exercises](https://github.com/exercism/v3-docs/blob/main/anatomy/tracks/concept-exercises.md) have been built
- A [test runner](https://github.com/exercism/v3-docs/blob/main/anatomy/track-tooling/test-runners/README.md) has been implemented
- A [representer](https://github.com/exercism/v3-docs/blob/main/anatomy/track-tooling/representers/README.md) has been implemented
- An [analyzer](https://github.com/exercism/v3-docs/blob/main/anatomy/track-tooling/analyzers/README.md) has been implemented

The status of these features is specified in the top-level `"status"` field in the track's `config.json`, as specified in [the spec](https://github.com/exercism/v3-docs/blob/master/anatomy/tracks/config-json.md#metadata).

The `"status"` field's values in the `config.json` file should be updated to reflect the status of the features (i.e. if they have been implemented).

## Tracking

https://github.com/exercism/v3-launch/issues/12
