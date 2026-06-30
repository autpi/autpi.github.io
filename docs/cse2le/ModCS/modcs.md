# ModCS Object - CSE2LE

The main "ModCS" object has a few extra functions in CSE2LE over the freeware autpi counterpart.

## REMOVED - ModCS.SetMag

ModCS.SetMag() is a dangerous function that has been removed in CSE2LE, as it could cause issues on other platforms / other options in the engine.

## ModCS.ShowMessageBox()

```lua
ModCS.ShowMessageBox(title, message)
```

Shows a message box over the window (usually for errors), with the `title` and `message` given.

## ModCS.PixelToScreenCoord()

```lua
ModCS.PixelToScreenCoord(value)
```

If `Enhanced Scrolling` is enabled, this function will correctly place a coordinate `value` on the screen as expected. This is used with `ModCS.Rect.Put()` and its variants.

## ModCS.SubpixelToScreenCoord()

```lua
ModCS.SubpixelToScreenCoord(value)
```

If `Enhanced Scrolling` is enabled, this function will correctly place a coordinate `value` in the world as expected. This is used with `ModCS.Rect.Put()` and its variants.

## ModCS.DisablePausing()

```lua
ModCS.DisablePausing()
```

This function will disable the ability to pause the game.

## ModCS.EnablePausing()

```lua
ModCS.EnablePausing()
```

This function will enable the ability to pause the game.

## ModCS.IsPausingEnabled()

```lua
ModCS.IsPausingEnabled()
```

This will return true if pausing is enabled.