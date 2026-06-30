# ModCS.Boss

The **ModCS.Boss class** represents Bosses (Also known as Map Bosses). Bosses are more hardcoded Npcs, basically.

Map bosses behave mostly the same as Npcs, using the exact same manipulation functions for the most part.

Below are functions specific to Map Bosses. Some Npc functions may be missing except for the essential ones.

## ModCS.Boss.GetByBufferIndex()

```lua
ModCS.Boss.GetByBufferIndex(index, ignorealive)
```

Directly gets `index` Boss from the Map Boss buffer. `ignorealive` is an optional boolean, that if true, will return a map boss even if the map boss is not alive/does not exist.

## ModCS.Boss.Copy()

```lua
ModCS.Boss.Copy(source, target)
```

Copies map boss `source` to `target`, meaning you can copy a map bosses current data to another (if you need to reuse it).

## ModCS.Boss.InitLife()

```lua
ModCS.Boss.InitLife()
```

Reset/remove the Boss health bar from the screen.

## ModCS.Boss.DrawLife()

```lua
ModCS.Boss.DrawLife()
```

Draws the Boss health bar on screen.

## ModCS.Boss.Set()

```lua
ModCS.Boss.Set(id)
```

Sets the boss of the current map to `id`.

| ID           | Boss                                 |
| ------------ | ------------------------------------ |
| `0`          | None                                 |
| `1`          | Omega                                |
| `2`          | Balfrog                              |
| `3`          | Monster X                            |
| `4`          | Core                                 |
| `5`          | Ironhead                             |
| `6`          | Twin Dragons                         |
| `7`          | Undead Core                          |
| `8`          | Heavy Press                          |
| `9`          | Ballos (Ball)                        |

## ModCS.Boss.ActMain()

```lua
ModCS.Boss.ActMain()
```

Runs all of the Boss action code -- Should probably only be ran in a case where you're overwriting a game mode.

## ModCS.Boss.TileHitCode()

```lua
ModCS.Boss.TileHitCode()
```

Runs the code for map bosses collision against tiles -- Should probably only be ran in a case where you're overwriting a game mode.

## ModCS.Boss.DrawMain()

```lua
ModCS.Boss.DrawMain(fx, fy)
```

Draws the map bosses on screen at the camera position `fx` and `fy`, making it function for a new game mode the user may add.