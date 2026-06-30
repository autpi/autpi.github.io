# ModCS.Arms

The **ModCS.Arms class** represents weapons that can be accessed from the inventory. The game has enough memory for 8 different weapons to be stored in the inventory.

A ModCS.Arms is userdata. You may access and edit the following values from it:

| Value           | Type                                 | Usage                                                        |
| --------------- | ------------------------------------ | ------------------------------------------------------------ |
| `id`           | Number (Casted to integer) | Type ID of the weapon.                |
| `level`         | Number (Casted to integer) | The weapon's level.                     |
| `exp`         | Number (Casted to integer) | The weapon's exp. Resets to 0 after every level up. |
| `ammo`         | Number (Casted to integer) | The weapon's current ammo count. |
| `max_ammo`    | Number (Casted to integer) | The maximum ammo of the weapon. If this is set to 0 the weapon will not have an ammo requirement. |

## ModCS.Arms.Add()

```lua
ModCS.Arms.Add(id, ammo)
```

Adds weapon of type `id` to the inventory. If a weapon of type `id` exists, update it.

`ammo` is an optional parameter. If specified, the added weapon will have maximum `ammo` ammo count.

## ModCS.Arms.Remove()

```lua
ModCS.Arms.Remove(id)
```

Removes weapon of type `id` from the inventory.

## ModCS.Arms.UseAmmo()

```lua
ModCS.Arms.UseAmmo(no)
```

`no` is an optional parameter, if not specified `no` will be set to 1.

Use `no` amount of ammo from the currently selected weapon. Returns false if the amount of ammo can't be used. Returns true otherwise.

## ModCS.Arms.AddAmmo()

```lua
ModCS.Arms.AddAmmo(no)
```

 Adds `no` amount of ammo to the currently selected weapon.

## ModCS.Arms.SwitchNext()

```lua
ModCS.Arms.SwitchNext()
```

Switches the currently selected weapon to the next one.

## ModCS.Arms.SwitchPrev()

```lua
ModCS.Arms.SwitchPrev()
```

Switches the currently selected weapon to the previous one.

## ModCS.Arms.SwitchFirst()

```lua
ModCS.Arms.SwitchFirst()
```

Switches the currently selected weapon to the first weapon in the inventory.

## ModCS.Arms.AddExp()

```lua
ModCS.Arms.AddExp(exp)
```

Adds `exp` amount of XP to the player.

## ModCS.Arms.RemoveExp()

```lua
ModCS.Arms.RemoveExp(exp)
```

Removes `exp` amount of XP from the player.

## ModCS.Arms.GetLevels()

```lua
ModCS.Arms.GetLevels(id)
```

Returns an array of the XP requirements for each level of weapon of type `id`. These values are read from the `data/arms_level.tbl`, or `data/arms_level.yaml` file. If no file exists, it will instead read from the game executable.

## ModCS.Arms.GetAmount()

```lua
ModCS.Arms.GetAmount()
```

Returns the amount of weapons that exist in the arms level table.

## ModCS.Arms.GetCurrent()

```lua
ModCS.Arms.GetCurrent()
```

Returns a ModCS.Arms of the currently selected weapon.

## ModCS.Arms.GetCurrentInvPos()

```lua
ModCS.Arms.GetCurrentInvPos()
```

Returns the inventory position of the currently selected weapon.

## ModCS.Arms.SetCurrentInvPos()

```lua
ModCS.Arms.SetCurrentInvPos(num)
```

Sets the inventory position of the currently selected weapon to `num`.

## ModCS.Arms.GetByID()

```lua
ModCS.Arms.GetByID(id)
```

Searched the inventory for a weapon with type ID `id`. If found, return a ModCS.Arms of that weapon. Otherwise return a nil value.

## ModCS.Arms.GetByInvPos()

```lua
ModCS.Arms.GetByInvPos(pos)
```

Return a ModCS.Arms of the weapon at inventory position `pos`.

## ModCS.Arms.CountBullet()

```lua
ModCS.Arms.CountBullet(id)
```

Returns how many bullets are on screen from Weapon `id`.

## ModCS.Arms.ResetCurrentEXP()

```lua
ModCS.Arms.ResetCurrentExp()
```

Resets currently selected weapon to Level 1, and removes all Exp from it.

## ModCS.Arms.IsCurrentMaxExp()

```lua
ModCS.Arms.IsCurrentMaxExp()
```

Returns true if the currently selected weapon is at Max Experience.

## ModCS.Arms.Clear()

```lua
ModCS.Arms.Clear()
```

Removes all weapons from the players inventory.

## ModCS.Arms.GetExpX()

```lua
ModCS.Arms.GetExpX()
```

Returns the X position variable used for the EXP hud at certain parts of hud/inventory code.

## ModCS.Arms.SetExpX()

```lua
ModCS.Arms.SetExpX(num)
```

Sets the X position variable used for the EXP hud at certain parts of hud/inventory code to the `num` value given.

## ModCS.Arms.ActMain()

```lua
ModCS.Arms.ActMain()
```

Runs the code for allowing the player to shoot their weapons -- Should probably only be ran in a case where you're overwriting a game mode, as this already runs normally. See the 'Weapon Shoot Code' segment for info on how to add new weapons instead.

## Weapon Shoot Code

The way Cave Story weapons work internally is a certain function runs on loop if the player is currently holding a certain type of weapon. ModCS allows you to override a weapon's shoot code. If a function in the `ModCS.Arms.Shoot` array is defined with the index `X` (where `X` is the Weapon Type ID you want to override) in your Lua script the game will run that function instead of the built-in shoot function.

??? Example
	```lua linenums="1"
	ModCS.Arms.Shoot[1] = function()
		-- ...
	end
	```