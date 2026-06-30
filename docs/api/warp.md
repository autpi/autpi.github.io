# ModCS.Warp

The **ModCS.Warp namespace** contains functions related to the teleporter menu.

## ModCS.Warp.Clear()

```lua
ModCS.Warp.Clear()
```

Resets and removes all teleporter/warp slots.

## ModCS.Warp.Add()

```lua
ModCS.Warp.Add(index, event)
```

Adds a teleporter slot to the `index` given, that runs the Tsc `event` when interacted with. The `index` just means where it is in the list of options, like how Egg Corridor is first in Cave Story, or how Sand Zone is third. 

## ModCS.Warp.Remove()

```lua
ModCS.Warp.Remove(index)
```

Removes a teleporter warp at the `index` given, if one is currently in that slot.
