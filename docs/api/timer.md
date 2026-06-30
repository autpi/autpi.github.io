# ModCS.Timer

The **ModCS.Timer namespace** contains functions related to Nikumaru / 290 counter.

## ModCS.Timer.Get()

```lua
ModCS.Timer.Get()
```

Returns the current value that the Nikumaru / 290 counter is at.

## ModCS.Timer.Set()

```lua
ModCS.Timer.Set(time)
```

Sets the current value for the Nikumaru / 290 counter to `time`.

## ModCS.Timer.Save()

```lua
ModCS.Timer.Save()
```

Saves the current time for the Nikumaru / 290 counter to a `290.rec` file.

## ModCS.Timer.Load()

```lua
ModCS.Timer.Load()
```

Sets a given lua variable to the `290.rec` timer saved. You can use `ModCS.Timer.Set()` after to set the actual timer to it, if wanted.

## ModCS.Timer.Put()

```lua
ModCS.Timer.Put(x, y)
```

Draws the Nikumaru / 290 counter at the given screen coordinates (`x`,`y`).