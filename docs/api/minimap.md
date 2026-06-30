# ModCS.MiniMap

The **ModCS.MiniMap namespace** contains functions related to the Map System.

## ModCS.MiniMap.ActLoop()

```lua
ModCS.MiniMap.ActLoop()
```

Puts the game into the MiniMap loop state. Set a local variable to this function, then, check if that variable is 0, 1, or 2. If 0, exit game. If 1, continue. If 2, reset to starting mode (original behavior).

## ModCS.MiniMap.Set()

```lua
ModCS.MiniMap.Set(flag)
```

Sets a 'MiniMap' flag. This is unused.

## ModCS.MiniMap.Get()

```lua
ModCS.MiniMap.Get()
```

Returns `true` if the current maps 'MiniMap' flag is set. This is unused.

## ModCS.MiniMap.Reset()

```lua
ModCS.MiniMap.Reset()
```

Reset the 'MiniMap' flags the game stores. These are completely unused.