# Mcattributes

This file stores any of the settings or attribtues related to the project. Which
uses universal determined keys along each project. Each tool/program may also
introduce each own set of keys, aslong as they are unique to the tool/program.
Other programs/tools simply ignore these keys. But when overwriting the file,
must keep the old keys from other tools or programs.

**Example**

```ini
diagnose=true
diagnose.objectives=true
diagnose.tags=true
diagnose.mcfunctions=true

world.area_used=0 0 0 1000 256 1000
```

## Properties

| Name                 | Type    | Description                                                                                                   |
| -------------------- | ------- | ------------------------------------------------------------------------------------------------------------- |
| diagnose             | boolean | Wheter or not the program should provide any diagnostics                                                      |
| diagnose.objectives  | boolean | Wheter or not the program should provide any diagnostics for scoreboard objectives existing or not            |
| diagnose.tags        | boolean | Wheter or not the program should provide any diagnostics for tags                                             |
| diagnose.mcfunctions | boolean | Wheter or not the program should provide any diagnostics for mcfunction file                                  |
| diagnose.json        | boolean | Wheter or not the program should provide any diagnostics for json file                                        |
| diagnose.lang        | boolean | Wheter or not the program should provide any diagnostics for language file                                    |
| world.area_used      | box     | The area defined as a box (`x y z x y z`) that this project confines itself to. Usefull for coordinate checks |
