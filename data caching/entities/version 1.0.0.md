# Entity cached data - 1.0.0

## Example file

```json
{
  "format_version": "1.0.0",
  "entities": [
    {
      "identifier": "minecraft:sheep",
      "families": ["animal", "mob"],
      "behavior": {
        "location": {
          "offset": 255,
          "uri": "./world/behavior_pack/bp/entities/sheep.entity.json"
        },
        "events": ["minecraft:spawned"],
        "animations": {
          "used": ["animation.sheep.dance", "controller.sheep.dance"],
          "defined": ["animation.dance", "controller.dance"]
        },
        "molang": {
          "variables": {
            "used": ["is_attacking"]
          },
          "queries":  {
            "used": ["modified_speed"]
          }
        }
      },
      "resource": {
        "location": {
          "offset": 255,
          "./world/resource_pack/rp/entities/sheep.entity.json"
        },
        "animations": ["animation.sheep.dance", "controller.sheep.dance"],
        "geometries": ["sheep"],
        "textures": ["texture/entities/sheep"],
        "render_controllers": ["controller.sheep.example"],
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
    }
  ]
}
```

## Structure

TODO write structure description
