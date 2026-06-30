# ModCS.Mod

The **ModCS.Mod namespace** contains functions related to customizing certain aspects of mods.

## ModCS.Mod.SetName()

```lua
ModCS.Mod.SetName(name)
```

Sets the window title of the game to `name`. This function will only work at top-level.

## ModCS.Mod.SetAuthor()

```lua
ModCS.Mod.SetAuthor(name)
```

Sets the author of game to `name`. Currently, the author only is used in debug printing for using `ModCS.AddEntity()`

## ModCS.Mod.SetOpening()

```lua
ModCS.Mod.SetOpening(no, x, y, eve, wait)
```

Use [Stage](/api/stage/) `no` for the opening sequence ([Game Mode](/api/game/#modcsgamegetmode) 1). `x` and `y` are the coordinates the camera focuses on. `eve` and `wait` are optional parameters.

If `eve` is specified [Event](/api/tsc/#events) `eve` will run once the opening sequence starts, otherwise Event 0 will run.

If `wait` is specified, wait `wait` ticks during the opening before transferring to the title screen. It will wait 500 ticks by default in vanilla Cave Story.

## ModCS.Mod.SetStart()

```lua
ModCS.Mod.SetStart(no, x, y, eve)
```

Sets the default New Game starting point. Parameters are the same as the [ModCS.Stage.Transfer() function](/api/stage/#modcsstagetransfer).

## ModCS.Mod.SetSpikeDamage()

```lua
ModCS.Mod.SetSpikeDamage(damage)
```

Sets the damage of the Spike tile type (Attribute 0x42) to `damage`.

## ModCS.Mod.SetBossHP()

```lua
ModCS.Mod.SetBossHP(no, hp)
```

Sets the life of the map boss `no` to the `hp` value given. The table for map bosses in vanilla is as such:

```
1: Omega
2: Balfrog
3: Monster X
4: Core
5: Ironhead
6: Dragon Sisters
7: Undead Core
8: Heavy Press
9: Ballos Ball (Phase 2)
10: Ballos Ball (Phase 4)
```

## ModCS.Mod.SetStartMyChar()

```lua
ModCS.Mod.SetStartMyChar(life, maxLife, direct)
```

Set the starting new-game state of the players current life to `life`, max life to `maxLife`, and direction to `direct`.

## ModCS.Mod.SetStartMode()

```lua
ModCS.Mod.SetStartMode(id)
```

Set the games boot-up / reset state to the mode `id`. The modes include:

```
1: Opening
2: Title
3: Gameplay
```

## ModCS.Mod.GetStartMode()

```lua
ModCS.Mod.GetStartMode()
```

Returns the games boot-up / reset state id.