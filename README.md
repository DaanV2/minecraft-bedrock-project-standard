# Minecraft Bedrock Project Standard

The goal of this standard is to unify multiple program, analyzers, generators or intellisense for example. This is accomplished through a universal
data caching format and universal project attribute. A secondary goal is also to provided sample files for unit testing

**Content**

- [Minecraft Bedrock Project Standard](#minecraft-bedrock-project-standard)
	- [Data Caching](#data-caching)
	- [Project Attribute](#project-attribute)
		- [McAttributes](#mcattributes)
		- [McDefinitions](#mcdefinitions)
		- [McIgnore](#mcignore)

## Data Caching

Any program or tool may during its operation and traversing of the files gather data, for better performance it sometimes better to save a summarized
version of this data to disk. So when the program starts up it already has data it can provided to the data will it might preform a rescan and save
that data for a latter use.

This standard provided a format of what that data at the bare minimum must contain, additional data is allowed, but can be overwritten by any other
tool. Any tool or program may create an unique subfolder with additional data for its own record keeping.

All data will be stored in a universal folder called `.minecraft-bedrock` there files can be found for each type of data by minecraft it self:

- [blocks.json](data%20caching/tags/version%201.0.0.md)
- [bp_animations.json](data%20caching/bp_animations/version%201.0.0.md)
- [bp_animation_controllers.json](data%20caching/bp_animation_controllers/version%201.0.0.md)
- [entities.json](data%20caching/entities/version%201.0.0.md)
- [families.json](data%20caching/families/version%201.0.0.md)
- [items.json](data%20caching/items/version%201.0.0.md)
- [names.json](data%20caching/names/version%201.0.0.md)
- [objectives.json](data%20caching/objectives/version%201.0.0.md)
- [particles.json](data%20caching/particles/version%201.0.0.md)
- [render_controller.json](data%20caching/render_controllers/version%201.0.0.md)
- [rp_animation.json](data%20caching/rp_animations/version%201.0.0.md)
- [rp_animation_controller.json](data%20caching/rp_animation_controllers/version%201.0.0.md)
- [sounds.json](data%20caching/sounds/version%201.0.0.md)
- [tags.json](data%20caching/tags/version%201.0.0.md)

A wider specification can be found in [data caching](data%20caching/data%20caching.md)

## Project Attribute

This standard will introduce 3 new file that will help with project definition, attributes, excluded/includes of folders/files and settings that deal
with project for minecraft bedrock.  
The file can be found in the root of the project. The following files will be added:

- [`.mcattribtues`](#mcattributes)
- [`.mcdefinitions`](#mcdefinitions)
- [`.mcignore`](#mcignore)

### McAttributes

The file with the name: `.mcattributes`. This file stores any of the settings or attribtues related to the project. Which uses universal determined
keys along each project. Each tool/program may also introduce each own set of keys, aslong as they are unique to the tool/program. Other
programs/tools simply ignore these keys. But when overwriting the file, must keep the old keys from other tools or programs.

A wider specification can be found in [McAttributes](McAttributes.md)

**Example**

```ini
diagnose=true
diagnose.objectives=true
diagnose.tags=true
diagnose.mcfunctions=true

world.area_used=0 0 0 1000 256 1000
```

---

### McDefinitions

This file specifies anything that is included in the project, but cannot be found in the project files itself, or not easly. At the same time the user
can also blacklist definition through this same project.

A wider specification can be found in [McDefinitions](McDefinitions.md)

**Example**

```ini
## I am a comment

## Tags used in the map
tag=initialized
tag=calculating
tag=enemy
tag=monster

## Tags to be black listed
tag=!Monster

## Objectives used in the map
objective=var
objective=coin
objective=foo

## Objectives blacklisted
objective=!Var
objective=!Coin

## Families
family=npc

## Families Blacklisted
family=!Npc

## Entity names
name=Steve

## Entity names blacklisted
name=!steve
```

---

### McIgnore

Based upon `.gitignore`. This file specifies through glob-patterns what files, folder to included/excluded from the project.

A wider specification can be found in [McIgnore](McIgnore.md)

**Example**

```ini
## This is a comment
## this will ignore the folders/file called Template
Template

## This will included file/folders that are in a folder called template and have the name and extension: settings.json
!Template/settings.json
```

---
