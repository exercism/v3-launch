# config.json migration

Note that for the below steps, we should detect if the track has already made this change (which the v3 tracks should have done) and use the v3 config.json values when update the v2 config.json file.

Any settings defined in the v3 config.json will take precedence of the v2 config.json.

1. Add a version property:

```json
"version": 3
```

2. Add online editor settings:

```json
"online_editor": {
  "indent_style": "space",
  "indent_size": 2
}
```

3. Rename the `"exercises"` property to `"practice"`

4. Create an `"exercises"` property and move the `"practice"` property to this property:

```json
"exercises": {
  "practice": [
    ...
  ]
}
```

5. Remove the `"core"`, `"auto_approve"`, and `"unlocked_by"` properties from the practice exercises

6. Add the `"name"` property to the practice exercises and pre-populate this with a titlelized version of the `"slug"` property

7. Add the `"prerequisites"` property to the practice exercises and set it to an empty array

8. Add an empty `"concept"` array property to the `"exercises"` property

```json
"exercises": {
  "concept": [],
  "practice": [
    ...
  ]
}
```

9. Move the `"foregone"` property to the `"exercises"` key:

```json
"exercises": {
  ...
  "foregone": [...]
}
```

10. Add a top-level `"concepts"` key, which is an array:

```json
"concepts": []
```

11. Add a top-level `"tags"` key, which is an array:

```json
"tags": []
```

12. Add a top-level `"key_features"` key, which is an array:

```json
"key_features": []
```

13. Add a top-level `"status"` key, which is an object containing properties with boolean values indicating if a v3 feature is implemented:

```json
"status": {
  "concept_exercises": true,
  "test_runner": true,
  "representer": false,
  "analyzer": false
}
```

14. Add a top-level `"slug"` key, which is a string containing the track's slug:

```json
"slug": "csharp"
```

15. Re-order the practice exercises using the following ordering:

1. Core exercises, retaining their existing ordering
2. Non-core exercises, ordered by the order of the core exercise that unlocks them, then by difficulty and then alphabetically.
3. Bonus exercises, ordered by difficulty then alphabetically.
