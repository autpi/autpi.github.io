# ModCS.Game

Functions related to the main game loop. Stored in the **ModCS.Game** object.

!!! Warning
	The main game loop does not include:

	- The inventory screen
	- The stage select screen
	- Minimap screen
	- Credits
	- Pause screen
	
	Functions such as [ModCS.Game.Act()](/api/game/#modcsgameact) and [ModCS.Game.Draw()](/api/game/#modcsgamedraw) will not run during these screens.

## ModCS.Game.GetMode()

```lua
ModCS.Game.GetMode()
```

Return a number that represents the current game mode.

| Value | Game mode         |
| ----- | ----------------- |
| 1     | Opening sequence. |
| 2     | Title screen.     |
| 3     | Action.           |

## ModCS.Game.IsNew()

```lua
ModCS.Game.IsNew()
```

Returns true if the 'New' option in the title screen was selected. Returns false otherwise.

## ModCS.Game.Init()

This function is called whenever a game mode is started.

??? Example
	This example will clear a variable `foo` on every game mode start.
	```lua linenums="1"
	function ModCS.Game.Init()
		-- Clear our foo variable
		foo = 0
	end
	```

## ModCS.Game.CanControl()

```lua
ModCS.Game.CanControl()
```

Returns false during a `<KEY` or `<PRI`. Returns true otherwise.

## ModCS.Game.CanAct()

```lua
ModCS.Game.CanAct()
```

Returns false during a `<PRI`. Returns true otherwise.

## ModCS.Game.GetGameFlags()

```lua
ModCS.Game.GetGameFlags()
```

Returns the current "Game Flags" value. This is the value checked for "CanControl()" and "CanAct()" as well.

## ModCS.Game.SetGameFlags()

```lua
ModCS.Game.SetGameFlags(num)
```

Set the current "Game Flags" value to `num`.

## ModCS.Game.Random()

```lua
ModCS.Game.Random(min, max)
```

Returns a random value between `min` and `max` using the games Random function.

## ModCS.Game.Random2()

```lua
ModCS.Game.Random2(min, max)
```

Returns a random value between `min` and `max`, using the games random function except multipling the input by 512, then giving the result divided by 512, to account for [Pixel Unit](/api/objects/pixel/) positions.

## ModCS.Game.Random3()

```lua
ModCS.Game.Random3(min, max)
```

Returns a random value between `min` and `max`, using the games random function except multipling the input by 512, then giving the result. To account for scenarios where you need to use [Pixel Unit](/api/objects/pixel/) style math but need the full integer value.

## ModCS.Game.SetBit()

```lua
ModCS.Game.SetBit(value, bit)
```

Sets a `bit` on `value`, with the usage of `value = ModCS.Game.SetBit(value, bit)`.

??? Example
	This example will set the players collision flag to "being in water".
	```lua linenums="1"
	ModCS.Player.hit_flag = ModCS.Game.SetBit(ModCS.Player.hit_flag, 0x100)
	```

## ModCS.Game.UnsetBit()

```lua
ModCS.Game.UnsetBit(value, bit)
```

Unsets a `bit` on `value`, with the usage of `value = ModCS.Game.UnsetBit(value, bit)`.

??? Example
	This example will unset the players collision flag from "being in water".
	```lua linenums="1"
	ModCS.Player.hit_flag = ModCS.Game.UnsetBit(ModCS.Player.hit_flag, 0x100)
	```

## ModCS.Game.CheckBit()

```lua
ModCS.Game.CheckBit(value, bit)
```

Checks if the `value` used has the `bit` set.

??? Example
	This example will check if the players collision flag is "being in water".
	```lua linenums="1"
	if (ModCS.Game.CheckBit(ModCS.Player.hit_flag, 0x100)) then
		print("woohoo! We're in water! So fun!")
	end
	```

## ModCS.Game.Act()

This function is called every frame before anything is updated or drawn in the main game loop.

??? Example
	This example will add 1 to a variable `foo` every frame.
	```lua linenums="1"
	function ModCS.Game.Act()
		-- Add 1 to our foo variable every frame
		foo = foo + 1
	end
	```

## ModCS.Game.Update()

This function is called every frame before anything is drawn in the main game loop. It differentiates from ModCS.Game.Act only on when exactly it's ran.

## ModCS.Game.Draw()

This function is called every frame after everything is drawn in the main game loop.

??? Example
	This example will draw the value of the variable `foo` using [ModCS.PutNumber](/api/modcs/#modcsputnumber).
	```lua linenums="1"
	function ModCS.Game.Draw()
		-- Draw the value of our variable
		ModCS.PutNumber(foo, 0, 0)
	end
	```

There are also other draw functions for other specific situations. They are listed here:

```lua
ModCS.Game.DrawBelowStageBack()
ModCS.Game.DrawAboveStageBack()
ModCS.Game.DrawBelowStageFront()
ModCS.Game.DrawAboveStageFront()
ModCS.Game.DrawBelowPlayer()
ModCS.Game.DrawAbovePlayer()
ModCS.Game.DrawBelowFade()
ModCS.Game.DrawAboveFade()
ModCS.Game.DrawBelowTextBox()
ModCS.Game.DrawAboveTextBox()
ModCS.Game.DrawHUD() -- Only draws when the hud is supposed to be drawn as well
```