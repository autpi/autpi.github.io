# Extra Options

Vanilla Cave Story has some extra functionality if certain empty files without file extension are present in the same directory as the EXE.

## Vanilla Options

- `s_reverse` - Swaps the weapon switch keys.
- `mute` - Unhides a context menu which opens a window for muting different Organya channels.
- `fps` - Enables a Framerate counter.

## AutPI Settings

AutPI contains various settings within the `mods/autpi` folder.

These include:

- `Write Tables on Boot (TBL)` - Writes `arms_level.tbl`, `bullet.tbl`, and `caret.tbl` from the game executable to the folder the game is stored in.
- `Write Tables on Boot (YAML)` - Writes `arms_level.yaml`, `bullet.yaml`, and `caret.yaml` from the game executable to the folder the game is stored in.
- `Replace Player Damage function` - Replaces the executables "Damage Player" function with a new one, allowing the user to also make their own Lua version of the Damage code.
- `Use Mode Overhaul` - Allows the user to create entirely new "Game Modes" in lua, at the cost of disabling the `ModCS.Game.SetMode()` function.
- `Debug Mode` - When pressing `Shift` and `F2` at the same time in-game, a Debug Menu will open to assist with modding.