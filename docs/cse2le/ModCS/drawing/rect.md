# ModCS.Rect (CSE2LE)

## ModCS.Rect.PutSC()

```lua
ModCS.Rect.PutSC(rect, x, y, surface, alpha)
ModCS.Rect.PutSC(rect, x, y, surface, surfaceto)
```

Exactly the same as `ModCS.Rect.Put()`, except `x` and `y` are automatically used with `ModCS.PixelToScreenCoord()`. Useful for `Enhanced Scrolling` being enabled, and wanting to draw an element to the screen (not world coordinates) without using `ModCS.PixelToScreenCoord()`.

## ModCS.Rect.PutExSC

```lua
ModCS.Rect.PutExSC(rect, viewrect, x, y, surface, alpha)
```

Exactly the same as `ModCS.Rect.PutEx()`, except `x` and `y` are automatically used with `ModCS.PixelToScreenCoord()`. Useful for `Enhanced Scrolling` being enabled, and wanting to draw an element to the screen (not world coordinates) without using `ModCS.PixelToScreenCoord()`.

## ModCS.Rect.PutAlpha()

```lua
ModCS.Rect.PutAlpha(rect, x, y, surface, alpha, angle, color, flip_x, flip_y)
```

This is copied from the SDL dll's `ModCS.SDL.PutAlpha()`. This will draw a rect on screen, with extra arguments for `alpha` (transparency, maximum is 255), `angle` (rotation, anywhere from 0-360 degrees), `color` (recoloring the sprite rect, `0xFFFFFF` for example), `flip_x` (boolean, will flip the rect horizontally), and `flip_y` (boolean, will flip the rect vertically).

## ModCS.Rect.PutAlphaSC()

```lua
ModCS.Rect.PutAlphaSC(rect, x, y, surface, alpha, angle, color, flip_x, flip_y)
```

Exactly the same as `ModCS.Rect.PutAlpha()`, except `x` and `y` are automatically used with `ModCS.PixelToScreenCoord()`. Useful for `Enhanced Scrolling` being enabled, and wanting to draw an element to the screen (not world coordinates) without using `ModCS.PixelToScreenCoord()`.