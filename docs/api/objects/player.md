# ModCS.Player

The **ModCS.Player global object** represents the player (Also known as My Character/ MYC).

ModCS.Player is userdata. You may access and edit the following values from it:

| Value        | Type                                 | Usage                                                        |
| ------------ | ------------------------------------ | ------------------------------------------------------------ |
| `x`          | [Pixel Unit](/api/objects/pixel/)    | The player's X position.                                     |
| `y`          | [Pixel Unit](/api/objects/pixel/)    | The player's Y position.                                     |
| `tgt_x`      | [Pixel Unit](/api/objects/pixel/)    | The player's camera X focus position.                        |
| `tgt_y`      | [Pixel Unit](/api/objects/pixel/)    | The player's camera Y focus position.                        |
| `index_x`    | [Pixel Unit](/api/objects/pixel/)    | The player's X camera movement from facing direction.      |
| `index_y`    | [Pixel Unit](/api/objects/pixel/)    | The player's Y camera movement from facing direction.      |
| `xm`         | [Pixel Unit](/api/objects/pixel/)    | X velocity of the Player.                                    |
| `ym`         | [Pixel Unit](/api/objects/pixel/)    | Y velocity of the Player.                                    |
| `ani_no`     | Number (Casted to integer)           | Animation frame value.                                       |
| `ani_wait`   | Number (Casted to integer)           | Animation timer value.                                       |
| `direct`     | [Direction](/api/objects/direction/) | The player's direction.                                      |
| `boost_fuel` | Number (Casted to integer)           | The fuel of the Player's [Booster](/api/objects/player/equip/). |
| `boost_sw` | Number (Casted to integer)           | Value used for the Player's [Booster](/api/objects/player/equip/), depends on type of boost. |
| `air`        | Number (Casted to integer)           | Air value of the player.                                     |
| `air_real`        | Number (Casted to integer)      | The 'real' Air value of the player. The default is divided by 10, which the HUD uses.                                     |
| `air_get`        | Number (Casted to integer)       | Extra value pertaining to air.                               |
| `fire_rate`  | Number (Casted to integer)           | Firerate of the players weapon ("Rensha")                    |
| `ammo_empty`  | Number (Casted to integer)           | Timer of the "empty" caret until it vanishes.               |
| `shock`      | Number (Casted to integer)           | The players invincibility value. Caps out at 255.            |
| `splash`     | Boolean                              | Set to 'true' if the player splashed in water.               |
| `down`       | Boolean                              | Set to 'true' if the player is facing down.                  |
| `up`         | Boolean                              | Set to 'true' if the player is facing up.                    |
| `ques`       | Boolean                              | If set to 'true', a question mark will spawn.                |
| `boost_sw`   | Number (Casted to integer)           | The boosters "direction". (Could be wrong.)                  |
| `unit`       | Number (Casted to integer)           | The players "unit" value. Used for different movement types. |
| `hit_flag`   | Number (Casted to integer)           | The players "collision" value. There's functions for this but if neccessary, this is here. |\
| `exp_wait`   | Number (Casted to integer)           | Wait timer for exp being added. (UI related)                 |
| `exp_count`  | Number (Casted to integer)           | The amount of exp used for a ValueView call in ActMyChar.    |
| `life`       | Number (Casted to integer)           | The players current health.                                  |
| `max_life`   | Number (Casted to integer)           | The players current maximum health.                          |
| `lifeBr`     | Number (Casted to integer)           | The players health used for health HUD.                      |
| `lifeBr_count` | Number (Casted to integer)         | A timer used for health HUD related things.                  |
| `bubble`     | Number (Casted to integer)           | Bubble flashing timer for Air Tank in water.                 |
| `star`       | Number (Casted to integer)           | Amount of whimsical stars in play.                           |
| `surf`       | Number (Casted to integer)           | The players surface ID. It doesn't do anything on it's own other than default to the correct ID of 16. |
| `x_cs`       | Number (Casted to integer)           | The player's X position (Multiplied by 512, the original Cave Story style.) |
| `y_cs`       | Number (Casted to integer)           | The player's Y position (Multiplied by 512, the original Cave Story style.) |
| `tgt_x_cs`   | Number (Casted to integer)           | The player's camera X focus position (Multiplied by 512, the original Cave Story style.) |
| `tgt_y_cs`   | Number (Casted to integer)           | The player's camera Y focus position (Multiplied by 512, the original Cave Story style.) |
| `index_x_cs` | Number (Casted to integer)           | The player's X camera movement from facing direction (Multiplied by 512, the original Cave Story style.) |
| `index_y_cs` | Number (Casted to integer)           | The player's Y camera movement from facing direction (Multiplied by 512, the original Cave Story style.) |
| `xm_cs`      | Number (Casted to integer)           | X velocity of the Player. (Multiplied by 512, the original Cave Story style.) |
| `ym_cs`      | Number (Casted to integer)           | Y velocity of the Player. (Multiplied by 512, the original Cave Story style.) |


## ModCS.Player.IsHit()

```lua
ModCS.Player.IsHit()
```

Returns true if the player is being hit. Returns false otherwise.

## ModCS.Player.IsLookingDown()

```lua
ModCS.Player.IsLookingDown()
```

Returns true if the player is looking down. Returns false otherwise.

## ModCS.Player.IsLookingUp()

```lua
ModCS.Player.IsLookingUp()
```

Returns true if the player is looking up. Returns false otherwise.

## ModCS.Player.GetLife()

```lua
ModCS.Player.GetLife()
```

Returns the player's current life points.

## ModCS.Player.AddLife()

```lua
ModCS.Player.AddLife(life)
```

Adds `life` to the player's life points.

## ModCS.Player.GetMaxLife()

```lua
ModCS.Player.GetMaxLife()
```

Returns the player's current maximum life points.

## ModCS.Player.AddMaxLife()

```lua
ModCS.Player.AddMaxLife(life)
```

Adds `life` to the player's max life points.

## ModCS.Player.Damage()

```lua
ModCS.Player.Damage(damage)
```

Damages the player by `damage`.

## ModCS.Player.DamageMyID()

```lua
ModCS.Player.DamageMyID(player, damage)
```

Same as `ModCS.Player.Damage()`, except it takes `player` as an argument. In the freeware version of autpi, this serves no active purpose. In CSE2LE, this will damage based on whatever that players ID is --> usually used with a npc's `tgt_mc` player object.

## ModCS.Player.SetRect()

```lua
ModCS.Player.SetRect(left, top, right, bottom)
ModCS.Player.SetRect(rect)
```

Sets the [Rect](/api/drawing/rect/) of the player to a Rect with `left`, `top`, `right`, `bottom`.

If a `rect` is specified, set the Rect of the player to that Rect instead.

## ModCS.Player.GetRect()

```lua
ModCS.Player.GetRect()
```

Returns the player's [Rect](/api/drawing/rect/).

## ModCS.Player.OffsetRect()

```lua
ModCS.Player.OffsetRect(left, top, right, bottom)
```

Adds `left`, `top`, `right`, `bottom` to the the `left`, `top`, `right`, `bottom` values of the [Rect](/api/drawing/rect/) of the player.

`right` and `bottom` are optional parameters. If they are not specified, `left` and `top` will be used in their place instead.

## ModCS.Player.SetViewbox()

```lua
ModCS.Player.SetViewbox(front, top, back, bottom)
ModCS.Player.SetViewbox(rangerect)
```

Sets the sprite offset of the Player to a [RangeRect](/api/objects/range/) with `front`, `top`, `back`, `bottom`.

If a `rangerect` is specified, set the sprite offset of the Player to that RangeRect instead.

## ModCS.Player.SetHitbox()

```lua
ModCS.Player.SetHitbox(front, top, back, bottom)
ModCS.Player.SetHitbox(rangerect)
```

Sets the hitbox of the Player to a [RangeRect](/api/objects/range/) with `front`, `top`, `back`, `bottom`.

If a `rangerect` is specified, set the hitbox of the Player to that RangeRect instead.

## ModCS.Player.GetViewbox()

```lua
ModCS.Player.GetViewbox()
```

Returns the sprite offset [RangeRect](/api/objects/range/) of the player.

## ModCS.Player.GetHitbox()

```lua
ModCS.Player.GetHitbox()
```

Returns the hitbox [RangeRect](/api/objects/range/) of the player.

## ModCS.Player.SetArmsYOffset()

```lua
ModCS.Player.SetArmsYOffset(offset)
```

Sets the vertical sprite offset of the weapon sprite next to the player to `offset`.

## ModCS.Player.SetCond()

```lua
ModCS.Player.SetCond(num)
```

Sets the player cond value to `num`. This is a "`bit`", so it's numbers like 1, 2, 4, 8, etc. This is not the same as NPC bits!

## ModCS.Player.UnsetCond()

```lua
ModCS.Player.UnsetCond(num)
```

Unsets the player cond value to `num`. This is a "`bit`", so it's numbers like 1, 2, 4, 8, etc. This is not the same as NPC bits!

## ModCS.Player.CheckCond()

```lua
ModCS.Player.CheckCond(num)
```

Checks if the players cond value contains `num`, it will return `true` if so.

## ModCS.Arms functions

The next functions in this list are copies of [ModCS.Arms](/api/inventory/arms/) functions, so you can use them inside the Player instead, or for compatibility between other engines that add multiplayer (CSE2LE).

## ModCS.Player.ArmsUseAmmo()

```lua
ModCS.Player.ArmsUseAmmo(no)
```

`no` is an optional parameter, if not specified `no` will be set to 1.

Use `no` amount of ammo from the currently selected weapon. Returns false if the amount of ammo can't be used. Returns true otherwise.

## ModCS.Player.ArmsAddAmmo()

```lua
ModCS.Player.ArmsAddAmmo(no)
```

 Adds `no` amount of ammo to the currently selected weapon.

## ModCS.Player.ArmsSwitchNext()

```lua
ModCS.Player.ArmsSwitchNext()
```

Switches the currently selected weapon to the next one.

## ModCS.Player.ArmsSwitchPrev()

```lua
ModCS.Player.ArmsSwitchPrev()
```

Switches the currently selected weapon to the previous one.

## ModCS.Player.ArmsSwitchFirst()

```lua
ModCS.Player.ArmsSwitchFirst()
```

Switches the currently selected weapon to the first weapon in the inventory.

## ModCS.Player.ArmsAddExp()

```lua
ModCS.Player.ArmsAddExp(exp)
```

Adds `exp` amount of XP to the player.

## ModCS.Player.ArmsRemoveExp()

```lua
ModCS.Player.ArmsRemoveExp(exp)
```

Removes `exp` amount of XP from the player.

## ModCS.Player.ArmsGetCurrent()

```lua
ModCS.Player.ArmsGetCurrent()
```

Returns a ModCS.Arms of the currently selected weapon.

## ModCS.Player.ArmsGetCurrentInvPos()

```lua
ModCS.Player.ArmsGetCurrentInvPos()
```

Returns the inventory position of the currently selected weapon.

## ModCS.Player.ArmsSetCurrentInvPos()

```lua
ModCS.Player.ArmsSetCurrentInvPos(num)
```

Sets the inventory position of the currently selected weapon to `num`.

## ModCS.Player.ArmsGetByID()

```lua
ModCS.Player.ArmsGetByID(id)
```

Searched the inventory for a weapon with type ID `id`. If found, return a ModCS.Arms of that weapon. Otherwise return a nil value.

## ModCS.Player.ArmsGetByInvPos()

```lua
ModCS.Player.ArmsGetByInvPos(pos)
```

Return a ModCS.Arms of the weapon at inventory position `pos`.

## ModCS.Player.ArmsCountBullet()

```lua
ModCS.Player.ArmsCountBullet(id)
```

Returns how many bullets are on screen from Weapon `id`.

## ModCS.Player.ArmsResetCurrentEXP()

```lua
ModCS.Player.ArmsResetCurrentExp()
```

Resets currently selected weapon to Level 1, and removes all Exp from it.

## ModCS.Player.ArmsIsCurrentMaxExp()

```lua
ModCS.Player.ArmsIsCurrentMaxExp()
```

Returns true if the currently selected weapon is at Max Experience.

## ModCS.Player.ArmsGetExpX()

```lua
ModCS.Player.ArmsGetExpX()
```

Returns the X position variable used for the EXP hud at certain parts of hud/inventory code.

## ModCS.Player.ArmsSetExpX()

```lua
ModCS.Player.ArmsSetExpX(num)
```

Sets the X position variable used for the EXP hud at certain parts of hud/inventory code to the `num` value given.

## ModCS.Player.ProcessAir()

```lua
ModCS.Player.ProcessAir()
```

Runs the vanilla games "air processing" function. This will already get ran if ModCS.Player.unit is 0.

## ModCS.Player.GetHitDamage()

```lua
ModCS.Player.GetHitDamage()
```

Returns the value used for damaging the player if the Damage Player function was replaced. Useless otherwise.

## ModCS.Player.Init()

```lua
ModCS.Player.Init()
```

Initializes the players data, like done when starting a new save.

## ModCS.Player.ActMain()

```lua
ModCS.Player.ActMain(canControl)
```

Runs the player action code, useful for creating a new game "mode", If `canControl` is true, then control will occur for the original function.

## ModCS.Player.AniMain()

```lua
ModCS.Player.AniMain(canControl)
```

Runs the player animation code, useful for creating a new game "mode". If `canControl` is true, then animation will occur for the original function.

## ModCS.Player.DrawMain()

```lua
ModCS.Player.DrawMain(fx, fy)
```

Draws the player on screen at the camera position `fx` and `fy`, making it function for a new game mode the user may add.

## ModCS.Player.ResetTileFlag()

```lua
ModCS.Player.ResetTileFlag()
```

Runs the code for resetting the players "hit_flag" for touching collision -- Should probably only be ran in a case where you're overwriting a game mode, and *before* `ModCS.Player.TileHitCode()` runs.

## ModCS.Player.TileHitCode()

```lua
ModCS.Player.TileHitCode()
```

Runs the code for the players collision against tiles -- Should probably only be ran in a case where you're overwriting a game mode.

## ModCS.Player.NpcHitCode()

```lua
ModCS.Player.NpcHitCode()
```

Runs the code for the players collision against npcs -- Should probably only be ran in a case where you're overwriting a game mode.

## ModCS.Player.BossHitCode()

```lua
ModCS.Player.BossHitCode()
```

Runs the code for the players collision against map bosses -- Should probably only be ran in a case where you're overwriting a game mode.

## ModCS.Player.DrawMain()

```lua
ModCS.Player.DrawMain(fx, fy)
```

Draws the player on screen at the camera position `fx` and `fy`, making it function for a new game mode the user may add.

## ModCS.Player.DrawLife()

```lua
ModCS.Player.DrawLife(flash)
```

Draws the players health HUD on screen. `flash` is a Boolean that when true, will flash the life hud when the player is damaged. This is useful if you're making a new game mode where this doesn't already run.

## ModCS.Player.DrawExp()

```lua
ModCS.Player.DrawExp(flash)
```

Draws the players exp HUD on screen. `flash` is a Boolean that when true, will flash the exp hud when the player is damaged. This is useful if you're making a new game mode where this doesn't already run.

## ModCS.Player.DrawAir()

```lua
ModCS.Player.DrawAir(x, y)
```

Draws the players air HUD at screen coordinates (`x`,`y`) while submerged in water. This is useful if you're making a new game mode where this doesn't already run.

## ModCS.Player.DrawArms()

```lua
ModCS.Player.DrawArms()
```

Draws the players weapons HUD on screen. This is useful if you're making a new game mode where this doesn't already run.