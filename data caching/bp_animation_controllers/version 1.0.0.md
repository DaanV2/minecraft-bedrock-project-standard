# Behaviorpack animation controllers - version 1.0.0

## Example

```json
{
  "format_version": "1.0.0",
  "controllers": [
    {
      "identifier": "animation.sheep.dance",
      "location": {
        "uri": "./world/behavior_packs/BP/functions/example.mcfunction",
        "offset": 255
      },
      "animations": {
        "used": ["dance"]
      },
      "events": {
        "used": ["minecraft:set_dance"]
      },
      "molang": {
        "variables": {
          "used": ["is_attacking"],
          "defined": ["is_dancing"]
        },
        "queries": {
          "used": ["modified_speed"]
        }
      }
    }
  ]
}
```

## Structure

TODO write structure description
