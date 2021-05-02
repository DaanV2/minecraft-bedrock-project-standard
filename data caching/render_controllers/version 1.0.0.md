# Render controllers- version 1.0.0

## Example

```json
{
  "format_version": "1.0.0",
  "controllers": [
    {
      "identifier": "render_controller.sheep.dance",
      "location": {
        "offset": 255,
        "uri": "./world/resource_pack/RP/render_controllers/controller.sheep.json"
      },
      "geometries": {
        "used": ["default"]
      },
      "materials": {
        "used": ["default", "alpha"]
      },
      "textures": {
        "used": ["default", "rave"]
      },
      "molang": {
        "variables": {
          "used": ["is_attacking"]
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
