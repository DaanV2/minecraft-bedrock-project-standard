# Minecraft Bedrock Project Standard

The goal of this standard is to unify multiple program, analyzers, generators or
intellisense for example. This is accomplished through an universal project
attribute. A secondary goal is also to provided sample files for unit testing

**Content**

- [Minecraft Bedrock Project Standard](#minecraft-bedrock-project-standard)
  - [Project Attribute](#project-attribute)
    - [McAttributes](#mcattributes)
    - [McDefinitions](#mcdefinitions)
    - [McIgnore](#mcignore)

## Project Attribute

This standard will introduce 3 new file that will help with project definition,
attributes, excluded/includes of folders/files and settings that deal with
project for minecraft bedrock.  
The file can be found in the root of the project. The following files will be
added:

- [Minecraft Bedrock Project Standard](#minecraft-bedrock-project-standard)
  - [Project Attribute](#project-attribute)
    - [McAttributes](#mcattributes)
    - [McDefinitions](#mcdefinitions)
    - [McIgnore](#mcignore)

### McAttributes

The file with the name: `.mcattributes`. This file stores any of the settings or
attribtues related to the project. Which uses universal determined keys along
each project. Each tool/program may also introduce each own set of keys, aslong
as they are unique to the tool/program. Other programs/tools simply ignore these
keys. But when overwriting the file, must keep the old keys from other tools or
programs.

A wider specification can be found in [McAttributes](mcattributes.md)

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

This file specifies anything that is included in the project, but cannot be
found in the project files itself, or not easly. At the same time the user can
also blacklist definition through this same project.

A wider specification can be found in [McDefinitions](mcdefinitions.md)

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

Based upon `.gitignore`. This file specifies through glob-patterns what files,
folder to included/excluded from the project.

A wider specification can be found in [McIgnore](mcignore.md)

**Example**

```ini
## This is a comment
## this will ignore the folders/file called Template
Template

## This will included file/folders that are in a folder called template and have the name and extension: settings.json
!Template/settings.json
```

---
