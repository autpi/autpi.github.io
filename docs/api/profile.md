# ModCS.Profile

The **ModCS.Mod namespace** contains functions related to the save files of mods.

## ModCS.Profile.Exists()

```lua
ModCS.Profile.Exists("ProfileName.dat")
```

Returns true if `ProfileName.dat` exists. Returns true if the standard Profile.dat exists if there is no string attached.

## ModCS.Profile.Save()

```lua
ModCS.Profile.Save("ProfileName.dat")
```

Saves the game when the function is called. The argument is optional, and will save as the standard Profile.dat if there is no string attached.

## ModCS.Profile.Load()

```lua
ModCS.Profile.Load("ProfileName.dat")
```

Loads the game when the function is called. The argument is optional, and will load the standard Profile.dat if there is no string attached.

## ModCS.Profile.GetName()

```lua
ModCS.Profile.GetName()
```

Returns the string of the most recent time the game saved, loaded, or checked for a save file.

## ModCS.Profile.DuringSave()

This function is called whenever the game is saved.

??? Example
	This example will print "Saving!" on every save.
	```lua linenums="1"
	function ModCS.Profile.DuringSave()
		print("Saving!")
	end
	```

## ModCS.Profile.DuringLoad()

This function is called whenever the game is loaded.

??? Example
	This example will print "Loading!" on every load.
	```lua linenums="1"
	function ModCS.Profile.DuringLoad()
		print("Loading!")
	end
	```