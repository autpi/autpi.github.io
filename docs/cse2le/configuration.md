# Mod Configuration

CSE2LE has multiple files pertaining to different things you can configure for your mod.

This file will go over multiple of them, and some of their options explaining how they work.

The files themselves also have their own default options, so you can learn more by reading the files.

## boot.ini

When the game is launched, boot.ini is checked first.

boot.ini simply holds an option for loading the mods data from a custom directory inside of the base data folder (`/(your mod path)/data`), via a "Mod Select" option.

CSE2LE has console ports, mainly Nintendo Switch and PlayStation Vita, in which the base data folder cannot be moved from its hardcoded location, so mods should assume that on those platforms, the mod select will always be used.

You may also use the mod select to create a collection of mods standalone for PC only, for example.

## mod.yaml

This file contains some important metadata about your mod, such as a name and a description. This file is used for the Mod Select menu that boot.ini can enable.

Even if you don't use the Mod Select menu on PC, you should fill out mod.yaml nonetheless, so that if someone does move your mod to a different platform, it's already setup.

## mods.ini

This file is loaded right at the start of your mod being loaded. This contains many important settings, such as:

- Window Name
- Multiplayer being enabled
- TextScript file encryption
- Filenames for different files the game loads
- Widescreen
- Allowing the game to run in the background
- Sprite Scale (2x resolution graphics)
- Boss, Bullet, Caret, Npc, and ValueView limits
- Certain DLL mods being built-in that you can enable (BKG, Layers, Lighting, etc.)
- Debug Mode for mod development
- Custom pause menu
- Different generic freeware hacks ported to simply toggles/value edits

## music.yaml

This yaml file is how you add custom music to your mod, whether it be organya or ogg.

You can add ogg files WiiWare style, where its 1 ogg file that loops, or 3ds style where you have an intro ogg file and a loop ogg.

More info can be seen inside of the file itself.

## sfx.yaml

This yaml file is how you add custom sound effects to your mod, whether it be pixtone or ogg/wav.

More info can be seen inside of the file itself.

## arms_level.tbl/yaml

This file (whether it be a .tbl, or the recommended/provided yaml file) contains the amount of Experience it takes to level up each Arms ID from Level 1 to 3.

## bullet.tbl/yaml

This file (whether it be a .tbl, or the recommended/provided yaml file) contains important data regarding all bullet properties, such as the damage it deals, the amount of frames its alive, and the hitbox size.

## caret.tbl/yaml

This file (whether it be a .tbl, or the recommended/provided yaml file) contains sprite offset for the left and top pixel coordinates of the carets.

Do note that one pixel is 512 units, since subpixels exist! So an 8 pixel offset would be `8 * 512`, or `4096`.

## pause_controls.txt

If the pause menu is enabled, this file contains the names of different control binding names.

## pause_names.txt

If the pause menu is enabled, this file contains the names of menu/option names.