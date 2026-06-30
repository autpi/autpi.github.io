# ModCS.Item

The **ModCS.Item class** represents non-weapon items that can be accessed from the inventory. The game has enough memory for 32 different items to be stored in the inventory.

A ModCS.Item is userdata. You may access and edit the following values from it:

| Value           | Type                                 | Usage                                                        |
| --------------- | ------------------------------------ | ------------------------------------------------------------ |
| `id`           | Number (Casted to integer) | Type ID of the item.           |

## ModCS.Item.Add()

```lua
ModCS.Item.Add(id)
```

Adds item of type `id` to the inventory.

## ModCS.Item.Remove()

```lua
ModCS.Item.Remove(id)
```

 Removes item of type `id` from the inventory.

## ModCS.Item.GetByID()

```lua
ModCS.Item.GetByID(id)
```

Searched the inventory for an item with type ID `id`. If found, return a ModCS.Item of that item. Otherwise return a nil value.

## ModCS.Item.GetByInvPos()

```lua
ModCS.Item.GetByInvPos(pos)
```

Return a ModCS.Item of the item at inventory position `pos`.

## ModCS.Item.GetCurrentInvPos()

```lua
ModCS.Item.GetCurrentInvPos()
```

Returns the inventory position of the currently selected item.

## ModCS.Item.SetCurrentInvPos()

```lua
ModCS.Item.SetCurrentInvPos(num)
```

Sets the inventory position of the currently selected item to `num`.

## ModCS.Item.Clear()

```lua
ModCS.Item.Clear()
```

Removes all items from the players inventory.

## ModCS.Item.InvLoop()

```lua
ModCS.Item.InvLoop()
```

Puts the game into the Inventory loop state. Set a local variable to this function, then, check if that variable is 0, 1, or 2. If 0, exit game. If 1, continue. If 2, reset to starting mode (original behavior).

## ModCS.Item.PutTimer()

```lua
ModCS.Item.PutTimer(x, y)
```

Draws the Nikumaru / 290 Counter on screen at the screen coordinates (`x`,`y`). Useful if you're making a new game mode, as the vanilla gameplay mode already does this at (`16`,`8`).