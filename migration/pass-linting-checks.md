# Pass linting checks

The [configlet tool](https://github.com/exercism/configlet) has a `lint` command that checks if a track's configuration files are properly structured - both syntactically and semantically. Misconfigured tracks may not sync correctly, may look wrong on the website, or may present a suboptimal user experience, so configlet's guards play an important part in maintaining the integrity of Exercism.

We've updated configlet to work with v3 tracks, which have a different set of requirements than v2 tracks.

The full list of rules that are checked by the linter can be found in [this spec](https://github.com/exercism/v3-docs/blob/master/anatomy/tracks/configlet/linting.md).

Tracks must make sure they pass all the (v3 track) checks defined in `configlet lint`.

## Tracking

https://github.com/exercism/v3-launch/issues/3
