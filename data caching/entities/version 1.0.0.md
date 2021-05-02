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
        "location": { "offset": 255, "uri": "./world/behavior_pack/bp/entities/sheep.entity.json" },
        "events": ["minecraft:spawned"],
        "animations": ["animation.sheep.dance", "controller.sheep.dance"],
        "molang": {
          "variables_used": ["is_attacking"],
          "queries_used": ["modified_speed"]
        }
      },
      "resource": {
        "location": { "offset": 255, "./world/resource_pack/rp/entities/sheep.entity.json" },
        "animations": ["animation.sheep.dance", "controller.sheep.dance"],
        "geometries": ["sheep"],
        "textures": ["texture/entities/sheep"],
        "render_controllers": ["controller.sheep.example"],
        "molang": {
          "variables_used": ["is_attacking"],
          "variables_defined": ["is_dancing"],
          "queries_used": ["modified_speed"]
        }
      }
    }
  ]
}
```

## Structure

TODO write structure description