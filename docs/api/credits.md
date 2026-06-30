# ModCS.Credits

The **ModCS.Credits namespace** contains functions related to the End Credits sequence.

## ModCS.Credits.Start()

```lua
ModCS.Credits.Start()
```

Begins the games Credits sequence, exactly like how `<CRE` would do it.

## ModCS.Credits.ActMain()

```lua
ModCS.Credits.ActMain()
```

Runs the main credits action code, handling the script and whatnot. Useful if creating a new game mode that doesn't already have this.

## ModCS.Credits.ActImg()

```lua
ModCS.Credits.ActImg()
```

Runs the credits action code for the large images that appear on the side. Useful if creating a new game mode that doesn't already have this.

## ModCS.Credits.ActCast()

```lua
ModCS.Credits.ActCast()
```

Runs the credits action code for the games 'cast' that appears on the side. Useful if creating a new game mode that doesn't already have this.

## ModCS.Credits.DrawImg()

```lua
ModCS.Credits.DrawImg()
```

Draws the large credits images on screen. Useful if creating a new game mode that doesn't already have this.

## ModCS.Credits.DrawCast()

```lua
ModCS.Credits.DrawCast()
```

Draws the games 'cast' that appear on the side. Useful if creating a new game mode that doesn't already have this.