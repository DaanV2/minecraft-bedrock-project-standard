# Data caching

Any program or tool may during its operation and traversing of the files gather data, for better performance it sometimes better to save a summarized
version of this data to disk. So when the program starts up it already has data it can provided to the data will it might preform a rescan and save
that data for a latter use.

This standard provided a format of what that data at the bare minimum must contain, additional data is allowed, but can be overwritten by any other
tool. Any tool or program may create an unique subfolder with additional data for its own record keeping.

All data will be stored in a universal folder called `.minecraft-bedrock`. there files can be found for each type of data by minecraft itself.

Like minecraft they carry a `format_version` property to define any possible future related changes

- [blocks.json](tags/version%201.0.0.md)
- [bp_animations.json](bp_animations/version%201.0.0.md)
- [bp_animation_controllers.json](bp_animation_controllers/version%201.0.0.md)
- [entities.json](entities/version%201.0.0.md)
- [families.json](families/version%201.0.0.md)
- [items.json](items/version%201.0.0.md)
- [names.json](names/version%201.0.0.md)
- [objectives.json](objectives/version%201.0.0.md)
- [particles.json](particles/version%201.0.0.md)
- [render_controller.json](render_controllers/version%201.0.0.md)
- [rp_animation.json](rp_animations/version%201.0.0.md)
- [rp_animation_controller.json](rp_animation_controllers/version%201.0.0.md)
- [sounds.json](sounds/version%201.0.0.md)
- [tags.json](tags/version%201.0.0.md)
