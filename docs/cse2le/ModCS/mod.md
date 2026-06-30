# ModCS.Mod (CSE2LE)

The **ModCS.Mod namespace** contains functions related to customizing certain aspects of mods.

CSE2LE contains some extra functions. However, the default freeware modcs functions are also available of course.

## ModCS.Mod.SetVersion()

```lua
ModCS.Mod.SetVersion(v1, v2, v3, v4)
```

This sets the version shown on the title screen in Cave Story, by default it is `1, 0, 0, 6`.

## ModCS.Mod.GetFPS()

```lua
ModCS.Mod.GetFPS()
```

This will return what framerate the game is currently set to run at. If it's set to `-1`, that simply means that the user hasn't overridden it and the game is handling it.

## ModCS.Mod.SetFPS()

```lua
ModCS.Mod.SetFPS(rate)
```

This will set the current framerate of the game to `rate`. If you're just swapping between 50/60fps, it's recommended to use `ModCS.Mod.Toggle60fps()` instead.

## ModCS.Mod.ResetFPS()

```lua
ModCS.Mod.ResetFPS()
```

This will reset the games framerate to the original rate it was running at if `ModCS.Mod.SetFPS()` was used.

## ModCS.Mod.Is60fps()

```lua
ModCS.Mod.Is60fps()
```

This will return true if the built-in 60fps functionality is enabled.

## ModCS.Mod.Toggle60fps()

```lua
ModCS.Mod.Toggle60fps(should)
```

This function is built-into freeware modcs as well, but instead of patching the game it simply toggles it in CSE2LE. `should` is a boolean, if true, 60fps will be enabled. If not true, it will instead be set to 50fps like freeware.

## ModCS.Mod.IsIntegerScaled()

```lua
ModCS.Mod.IsIntegerScaled()
```

This will return true if Integer Scaling is enabled, making the window only be able to resize to proper clean pixel upscales of the resolution the game is set to. Example being 320x240 would scale to 2x size if the window is at least the size of 640x480.

## ModCS.Mod.ToggleIntegerScaling()

```lua
ModCS.Mod.ToggleIntegerScaling(should)
```

This will enable Integer Scaling if `should` is set to true.

## ModCS.Mod.IsSmoothScrolling()

```lua
ModCS.Mod.IsSmoothScrolling()
```

This will return true if Smooth Scrolling is enabled. Smooth Scrolling makes the camera movement smoother, only if `Enhanced Scrolling` is enabled in `mods.ini`. The one downside is that anytime you use `ModCS.Rect.Put()` or one of its variants, you'll need to surround the x/y coordinate in a `ModCS.PixelToScreenCoord(x/y)` or `ModCS.SubpixelToScreenCoord(x/y)` depending on the situation. For freeware accuracy, you can disable `Enhanced Scrolling` and not have to worry about this.

## ModCS.Mod.ToggleSmoothScrolling()

```lua
ModCS.Mod.ToggleSmoothScrolling(should)
```

This will enable Smooth Scrolling if `should` is set to true.

## ModCS.Mod.GetPlatform()

```lua
ModCS.Mod.GetPlatform()
```

This function will return a string of what platform the game is being ran on. These include:

- Windows
- macOS
- Linux
- FreeBSD
- Switch
- Vita

## ModCS.Mod.IsConsole()

```lua
ModCS.Mod.IsConsole()
```

This function will return true if the game is being ran on console, that being Nintendo Switch or PlayStation Vita.