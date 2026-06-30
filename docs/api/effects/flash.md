# ModCS.Flash

The **ModCS.Flash namespace** contains functions related to the flash effects.

## ModCS.Flash.Init()

```lua
ModCS.Flash.Init()
```

Resets the Flash effect, like done when starting a new save.

## ModCS.Flash.ActMain()

```lua
ModCS.Flash.ActMain(fx, fy)
```

Runs the Flash act code at the camera position `fx` and `fy`, making it function for a new game mode the user may add.

## ModCS.Flash.DrawMain()

```lua
ModCS.Flash.DrawMain()
```

Draws the Flash on screen, making it function for a new game mode the user may add.

## ModCS.Flash.Spawn()

```lua
ModCS.Flash.Spawn(explosion, x, y)
```

Spawns a flash effect on screen. `explosion`, `x`, and `y` are optional parameters. `explosion` is a Boolean. If true, then a boss explosion effect will spawn at coordinates `x` and `y`.

## ModCS.Flash.Reset()

```lua
ModCS.Flash.Reset()
```

Resets the flash state -- Used during a ModCS.Stage.Transfer().