# Behaviorpack animation controllers - version 1.0.0

## Example

```json
{
  "format_version": "1.0.0",
  "controllers": [
    {
      "identifier": "animation.sheep.dance",
      "location": { "uri": "./world/behavior_packs/BP/functions/example.mcfunction", "offset": 255 },
      "animations_used": ["dance"],
      "events_used": ["minecraft:set_dance"],
      "molang": {
        "variables_used": ["is_attacking"],
        "variables_defined": ["is_dancing"],
        "queries_used": ["modified_speed"]
      }
    }
  ]
}
```

## Structure

TODO write structure description
