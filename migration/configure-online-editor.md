# Configure online editor

In Exercism v3, students can now choose to work on exercises directly from their browser, instead of having to download exercises to their local machine. The track-specific settings for the in-browser editor are defined in the top-level `"online_editor"` field in the track's `config.json` file. This field is defined as an object with two fields:

- `"indent_style"`: the indent style, either "space" or "tab".
- `"indent_size"`: the indent size, which is an integer (e.g. 4).

You can find a full description of these fields in [the spec](https://github.com/exercism/v3-docs/blob/master/anatomy/tracks/config-json.md#metadata).

The `"online_editor"` field should be updated to correspond to the track's best practices regarding indentation.

## Tracking

https://github.com/exercism/v3-launch/issues/2
