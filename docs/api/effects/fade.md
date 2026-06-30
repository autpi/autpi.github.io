# ModCS.Fade

The **ModCS.Fade namespace** contains functions related to the fade effects.

## ModCS.Fade.Init()

```lua
ModCS.Fade.Init()
```

Resets the Fading effect, like done when starting a new save.

## ModCS.Fade.SetMask()

```lua
ModCS.Fade.SetMask()
```

Puts the fade mask on screen immediately (makes the screen faded out).

## ModCS.Fade.Clear()

```lua
ModCS.Fade.Clear()
```

Removes the fade mask on screen, immediately making the screen visible.

## ModCS.Fade.ActMain()

```lua
ModCS.Fade.ActMain()
```

Runs the Fading act code, making it function for a new game mode the user may add.

## ModCS.Fade.DrawMain()

```lua
ModCS.Fade.DrawMain()
```

Draws the Fade effect on screen, making it function for a new game mode the user may add.

## ModCS.Fade.Out()

```lua
ModCS.Fade.Out(dir)
```

Start a fade out, in direction `dir`.

## ModCS.Fade.In()

```lua
ModCS.Fade.In(dir)
```

Start a fade in, in direction `dir`.

## ModCS.Fade.Active()

```lua
ModCS.Fade.IsActive()
```

Returns `true` if a fade is currently happening.