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

13. Add a top-level `"v3_ready"` key, which is a boolean value that is set to `true` if the track is a v3 track, and otherwise set to `false`:

```json
"v3_ready": true
```
