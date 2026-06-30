# ModCS.Camera

The **ModCS.Camera namespace** contains functions related to the in-game camera.

## ModCS.Camera.SetTarget()

```lua
ModCS.Camera.SetTarget(obj)
```

Sets the camera target to Game object `obj` (Can be [ModCS.Player](/api/objects/player/), a [ModCS.Npc](/api/objects/npc/), a [ModCS.Caret](/api/objects/caret/) or a [ModCS.Bullet](/api/objects/bullet/))

## ModCS.Camera.SetDelay()

```lua
ModCS.Camera.SetDelay(x)
```

Sets the camera delay to `x` (Default is 16).

## ModCS.Camera.Reset()

```lua
ModCS.Camera.Reset()
```

Resets the camera position to the player.

## ModCS.Camera.GetXPos()

```lua
ModCS.Camera.GetXPos()
```

Returns the camera's X axis position in [Pixel Units](/api/objects/pixel/).

## ModCS.Camera.GetYPos()

```lua
ModCS.Camera.GetYPos()
```

Returns the camera's Y axis position in [Pixel Units](/api/objects/pixel/).

## ModCS.Camera.GetRealXPos()

```lua
ModCS.Camera.GetRealXPos()
```

Returns the camera's proper X axis position as a real integer number.

## ModCS.Camera.GetRealYPos()

```lua
ModCS.Camera.GetRealYPos()
```

Returns the camera's proper Y axis position as a real integer number.

## ModCS.Camera.SetQuake()

```lua
ModCS.Camera.SetQuake(time)
```

Makes the camera shake for `time` ticks.

## ModCS.Camera.SetAltQuake()

```lua
ModCS.Camera.SetAltQuake(time)
```

Makes the camera shake more violently for `time` ticks.

## ModCS.Camera.ResetQuake()

```lua
ModCS.Camera.ResetQuake()
```

Resets both the camera quake / alt quake.

## ModCS.Camera.SetPlayerFocus()

```lua
ModCS.Camera.SetPlayerFocus(time)
```

Makes the camera focus on the player in `time` ticks. Default would be 16.

## ModCS.Camera.ActMain()

```lua
ModCS.Camera.ActMain()
```

Runs the code for making the camera actually move around -- Should probably only be ran in a case where you're overwriting a game mode.