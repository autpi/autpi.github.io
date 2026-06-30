# ModCS.Const - Constant Variables

There are times where you may want to quickly pull (but not edit) certain values used in Cave Story for different things, such as the ARMS, ITEM, or NPC limit.

Below is a table of Constants you can pull, via `ModCS.Const.x`, where `x` is the constant from the table below.

??? Example
	This example will draw the NPC limit in the top-left corner of the screen using ModCS.PutNumber().
	```lua linenums="1"
	function ModCS.Game.Draw()
		ModCS.PutNumber(ModCS.Const.NPC_MAX, 0, 0)
	end
	```

Please note, that some of the "Values" in this table can change depending on what engine, or what other dlls you are using to modify your game.

| Constant                               | Value | Description                                                                                            |
| -------------------------------------- | ----- | ------------------------------------------------------------------------------------------------------ |
| `ARMS_MAX`                             |  `8`  | The maximum amount of Weapons the Player can hold.                                                     |
| `BOSS_MAX`                             | `20`  | The maximum amount of Map Bosses in the games `gBoss` object, including boss-related entities.         |
| `BULLET_MAX`                           | `64`  | The maximum amount of Bullets allowed in the world.                                                    |
| `CARET_MAX`                            | `64`  | The maximum amount of Carets allowed in the world.                                                     |
| `ITEM_MAX`                             | `32`  | The maximum amount of Items the Player can hold.                                                       |
| `MAX_STRIP`                            | `16`  | The maximum amount of 'Casts' allowed on screen during the credits sequence.                           |
| `NPC_MAX`                              | `512` | The maximum amount of Npcs allows in the world.                                                        |
| `SE_MAX`                               | `160` | The maximum amount of Sound Effects.                                                                   |
| `STAGE_MAX`                            |  `8`  | The maximum amount of Teleporter warp locations.                                                       |
| `MODE_OPENING`                         |  `1`  | The "game mode" ID for the Opening mode.                                                               |
| `MODE_TITLE`                           |  `2`  | The "game mode" ID for the Title Screen mode.                                                          |
| `MODE_ACTION`                          |  `3`  | The "game mode" ID for the Gameplay / Action mode.                                                     |
| `BACKGROUND_TYPE_STATIONARY`           |  `0`  | Background type ID for the background standing still.                                                  |
| `BACKGROUND_TYPE_MOVE_DISTANT`         |  `1`  | Background type ID for the background following distantly.                                             |
| `BACKGROUND_TYPE_MOVE_NEAR`            |  `2`  | Background type ID for the background following closer to the foreground.                              |
| `BACKGROUND_TYPE_WATER`                |  `3`  | Background type ID for drawing the water texture on screen moving up and down with water level.        |
| `BACKGROUND_TYPE_BLACK`                |  `4`  | This background type ID does nothing, however is used in the Stage Table from rooms with no back.      |
| `BACKGROUND_TYPE_AUTOSCROLL`           |  `5`  | Background type ID autoscrolls the background left, like during the Ironhead boss fight.               |
| `BACKGROUND_TYPE_CLOUDS_WINDY`         |  `6`  | Background type ID autoscrolls layers of the background, used for Outer Wall.                          |
| `BACKGROUND_TYPE_CLOUDS`               |  `7`  | Background type ID autoscrolls layers of the background, used for Balcony.                             |
| `CARET_NULL`                           |  `0`  | Caret type ID that does nothing.                                                                       |
| `CARET_BUBBLE`                         |  `1`  | Caret type ID used for Gunfish/Lava droplet effects.                                                   |
| `CARET_PROJECTILE_DISSIPATION`         |  `2`  | Caret type ID used for when a bullet disappears, along with other effects.                             |
| `CARET_SHOOT`                          |  `3`  | Caret type ID used for when a bullet is fired from the Players weapon.                                 |
| `CARET_SNAKE_AFTERIMAGE`               |  `4`  | Caret type ID used for the Snake weapons "afterimage" effect.                                          |
| `CARET_ZZZ`                            |  `5`  | Caret type ID used for the Hermit Gunsmith's snoring effect.                                           |
| `CARET_SNAKE_AFTERIMAGE_DUPLICATE`     |  `6`  | Duplicate of the `CARET_SNAKE_AFTERIMAGE` id, for some reason.                                         |
| `CARET_EXHAUST`                        |  `7`  | Caret type ID used for the Booster 0.8 / 2.0 exhaust when boosting.                                    |
| `CARET_DROWNED_QUOTE`                  |  `8`  | Caret type ID used for when the Player drowns -- The "MyChar" sprite is replaced with this.            |
| `CARET_QUESTION_MARK`                  |  `9`  | Caret type ID used for when the Player interacts with nothing.                                         |
| `CARET_LEVEL_UP`                       |  `10` | Caret type ID used for when the Player's weapon levels up/down. `DIR_LEFT` is up, `DIR_RIGHT` is down. |
| `CARET_HURT_PARTICLES`                 |  `11` | Caret type ID used for when a Npc/Boss is hurt. |
| `CARET_EXPLOSION`                      |  `12` | Caret type ID used for a explosion-style effect, like when the Player dies. |
| `CARET_TINY_PARTICLES`                 |  `13` | Caret type ID used for the tiny particles that appear when the Player bonks the ceiling, for example. |
| `CARET_UNKNOWN`                        |  `14` | Caret type ID 'unused'. Code exists for this caret, but it's nonfunctional and unknown what it was for. |
| `CARET_PROJECTILE_DISSIPATION_TINY`    |  `15` | Caret type ID used for a tinier version of the projectile dissipation effect, used for Bubbler/Bubbline. |
| `CARET_EMPTY`                          |  `16` | Caret type ID used for when the Players weapon runs out of ammo. |
| `CARET_PUSH_JUMP_KEY`                  |  `17` | Caret type ID unused, shows 'PUSH JUMP KEY' on screen. It does not despawn. |
| `CREDIT_MODE_STOP`                     |  `0`  | ??? |
| `CREDIT_MODE_SCROLL_READ`              |  `1`  | ??? |
| `CREDIT_MODE_SCROLL_WAIT`              |  `2`  | ??? |
| `DIR_LEFT`                             |  `0`  | Direction ID for the 'Left' direction in most cases. |
| `DIR_UP`                               |  `1`  | Direction ID for the 'Up' direction in most cases. |
| `DIR_RIGHT`                            |  `2`  | Direction ID for the 'Right' direction in most cases. This is also frequently used as a "Alternate Mode" option. |
| `DIR_DOWN`                             |  `3`  | Direction ID for the 'Down' direction in most cases. |
| `DIR_AUTO`                             |  `4`  | Direction ID for the 'Center' fade effect, as well as making an Npc face the Player depending on where the Player is.  |
| `DIR_OTHER`                            |  `5`  | ??? |
| `EQUIP_BOOSTER_0_8`                    |  `1`  | Player Equipment ID for the Booster 0.8. |
| `EQUIP_MAP`                            |  `2`  | Player Equipment ID for the Map System. |
| `EQUIP_ARMS_BARRIER`                   |  `4`  | Player Equipment ID for the Arms Barrier. |
| `EQUIP_TURBOCHARGE`                    |  `8`  | Player Equipment ID for the Turbocharge. |
| `EQUIP_AIR_TANK`                       |  `16` | Player Equipment ID for the Air Tank. |
| `EQUIP_BOOSTER_2_0`                    |  `32` | Player Equipment ID for the Booster 2.0. |
| `EQUIP_MIMIGA_MASK`                    |  `64` | Player Equipment ID for the Mimiga Mask. |
| `EQUIP_WHIMSICAL_STAR`                 | `128` | Player Equipment ID for the Whimsical Star. |
| `EQUIP_NIKUMARU_COUNTER`               | `256` | Player Equipment ID for the Nikumaru/290 counter. |
| `ESCRETURN_exit`                       |  `0`  | Used when telling the game to quit. |
| `ESCRETURN_continue`                   |  `1`  | Used when telling the game to continue what it was doing previously. |
| `ESCRETURN_restart`                    |  `2`  | Used when telling the game to restart. |
| `FLASH_MODE_EXPLOSION`                 |  `1`  | 'Flash' ID for a explosion type flash effect spawning. |
| `FLASH_MODE_FLASH`                     |  `2`  | 'Flash' ID for the screen flashing. |
| `ILLUSTRATION_ACTION_IDLE`             |  `0`  | ??? |
| `ILLUSTRATION_ACTION_SLIDE_IN`         |  `1`  | ??? |
| `ILLUSTRATION_ACTION_SLIDE_OUT`        |  `2`  | ??? |
| `KEY_LEFT`                             |  `1`  | Key ID for the left movement key. |
| `KEY_RIGHT`                            |  `2`  | Key ID for the right movement key. |
| `KEY_UP`                               |  `4`  | Key ID for the up movement key. |
| `KEY_DOWN`                             |  `8`  | Key ID for the down movement key. |
| `KEY_MAP`                              |  `16` | Key ID for the Map System. |
| `KEY_X`                                |  `32` | Key ID for the X key. |
| `KEY_Z`                                |  `64` | Key ID for the Z key. |
| `KEY_ARMS`                             | `128` | Key ID for the "Switching Arms Right" key. |
| `KEY_ARMSREV`                          | `256` | Key ID for the "Switching Arms Left" key. |
| `KEY_SHIFT`                            | `512` | Key ID for the Left Shift key. |
| `KEY_F1`                               | `1024`| Key ID for the F1 key. |
| `KEY_F2`                               | `2048`| Key ID for the F2 key. |
| `KEY_ITEM`                             | `4096`| Key ID for the Inventory key. |
| `KEY_ESCAPE`                           |`32768`| Key ID for the Escape/Pause key. |
| `KEY_ALT_LEFT`                         |`65536`| Key ID for the alternative left key. |
| `KEY_ALT_DOWN`                         |`131072`| Key ID for the alternative down key. |
| `KEY_ALT_RIGHT`                        |`262144`| Key ID for the alternative right key. |
| `KEY_ALT_UP`                           |`1572864`| Key ID for the alternative up key. (L + Plus/Equals merged) |
| `KEY_L`                                |`524288`| Key ID for the 'L' key. |
| `KEY_PLUS`                             |`1048576`| Key ID for the 'Plus/Equals' key. |
| `NPC_SOLID_SOFT`                       |  `1`  | Npc bit flag for making the Npc softly push the Player out of its collision. |
| `NPC_IGNORE_TILE_44`                   |  `2`  | Npc bit flag for making the Npc ignore the "0x44" tile IDs collision. |
| `NPC_INVULNERABLE`                     |  `4`  | Npc bit flag for making the Npc unable to take damage, and use a special effect on hit. |
| `NPC_IGNORE_SOLIDITY`                  |  `8`  | Npc bit flag for making the Npc ignore tile collision. |
| `NPC_BOUNCY`                           |  `16` | Npc bit flag for making the Npc bouncy on top. |
| `NPC_SHOOTABLE`                        |  `32` | Npc bit flag used for making the Npc shootable by bullets. |
| `NPC_SOLID_HARD`                       |  `64` | Npc bit flag used for making the Npc solid, similar to a tile. |
| `NPC_REAR_AND_TOP_DONT_HURT`           | `128` | Npc bit flag used for ???. |
| `NPC_EVENT_WHEN_TOUCHED`               | `256` | Npc bit flag used for running a Tsc event when touched by the Player. |
| `NPC_EVENT_WHEN_KILLED`                | `512` | Npc bit flag used for running a Tsc event when killed instead of doing the normal death scenario. |
| `NPC_APPEAR_WHEN_FLAG_SET`             | `2048`| Npc bit flag used for making an Npc show up on room load when a Flag ID is set.                                     |
| `NPC_SPAWN_IN_OTHER_DIRECTION`         | `4096`| Npc bit flag used for making an Npc spawn with direction `DIR_RIGHT` instead of `DIR_LEFT`. |
| `NPC_INTERACTABLE`                     | `8192`| Npc bit flag used for making an Npc interactable for the Player. |
| `NPC_HIDE_WHEN_FLAG_SET`               |`16384`| Npc bit flag used for making an Npc disappear on room load when a Flag ID is set. |
| `NPC_SHOW_DAMAGE`                      |`32768`| Npc bit flag used for showing the damage 'ValueView' when the Npc is hit. |
| `MUS_SILENCE`                          |  `0`  | Music ID for nothing, silence. |
| `MUS_MISCHIEVOUS_ROBOT`                |  `1`  | Music ID for Mischievous Robot. |
| `MUS_SAFETY`                           |  `2`  | Music ID for Safety. |
| `MUS_GAME_OVER`                        |  `3`  | Music ID for 'Game Over'. |
| `MUS_GRAVITY`                          |  `4`  | Music ID for Gravity. |
| `MUS_ON_TO_GRASSTOWN`                  |  `5`  | Music ID for 'On to Grasstown!' |
| `MUS_MELTDOWN2`                        |  `6`  | Music ID for Meltdown 2. |
| `MUS_EYES_OF_FLAME`                    |  `7`  | Music ID for 'Eyes of Flame'. |
| `MUS_GESTATION`                        |  `8`  | Music ID for Gestation. |
| `MUS_MIMIGA_TOWN`                      |  `9`  | Music ID for Mimiga Town. |
| `MUS_GOT_ITEM`                         | `10`  | Music ID for the fanfare used when getting an item. |
| `MUS_BALROGS_THEME`                    | `11`  | Music ID for Balrogs Theme. |
| `MUS_CEMETERY`                         | `12`  | Music ID for Cemetery. |
| `MUS_PLANT`                            | `13`  | Music ID for Plant. |
| `MUS_PULSE`                            | `14`  | Music ID for Pulse. |
| `MUS_VICTORY`                          | `15`  | Music ID for the fanfare used for winning. |
| `MUS_GET_HEART_TANK`                   | `16`  | Music ID for the fanfare used for getting a life capsule. |
| `MUS_TYRANT`                           | `17`  | Music ID for Tyrant. |
| `MUS_RUN`                              | `18`  | Music ID for 'Run!' |
| `MUS_JENKA1`                           | `19`  | Music ID for Jenka 1. |
| `MUS_LABYRINTH_FIGHT`                  | `20`  | Music ID for Labyrinth Fight. |
| `MUS_ACCESS`                           | `21`  | Music ID for Access. |
| `MUS_OPPRESSION`                       | `22`  | Music ID for Oppression. |
| `MUS_GEOTHERMAL`                       | `23`  | Music ID for Geothermal. |
| `MUS_CAVE_STORY`                       | `24`  | Music ID for 'Cave Story'. |
| `MUS_MOONSONG`                         | `25`  | Music ID for Moonsong. |
| `MUS_HEROS_END`                        | `26`  | Music ID for Heros End. |
| `MUS_SCORCHING_BACK`                   | `27`  | Music ID for Scorching Back. |
| `MUS_QUIET`                            | `28`  | Music ID for Quiet. |
| `MUS_LAST_CAVE`                        | `29`  | Music ID for Last Cave. |
| `MUS_BALCONY`                          | `30`  | Music ID for Balcony. |
| `MUS_CHARGE`                           | `31`  | Music ID for Charge. |
| `MUS_LAST_BATTLE`                      | `32`  | Music ID for Last Battle. |
| `MUS_THE_WAY_BACK_HOME`                | `33`  | Music ID for 'The Way Back Home`. |
| `MUS_ZOMBIE`                           | `34`  | Music ID for Zombie. |
| `MUS_BREAK_DOWN`                       | `35`  | Music ID for Break Down. |
| `MUS_RUNNING_HELL`                     | `36`  | Music ID for Running Hell. |
| `MUS_JENKA2`                           | `37`  | Music ID for Jenka 2. |
| `MUS_LIVING_WATERWAY`                  | `38`  | Music ID for Living Waterway. |
| `MUS_SEAL_CHAMBER`                     | `39`  | Music ID for Seal Chamber. |
| `MUS_TOROKOS_THEME`                    | `40`  | Music ID for Toroko's theme. |
| `MUS_WHITE`                            | `41`  | Music ID for 'White'. |
| `SURFACE_ID_TITLE`                     |  `0`  | Surface ID for the Title screen image. |
| `SURFACE_ID_PIXEL`                     |  `1`  | Surface ID for the 'PIXEL' copyright image. |
| `SURFACE_ID_LEVEL_TILESET`             |  `2`  | Surface ID for the current rooms tileset. |
| `SURFACE_ID_FADE`                      |  `6`  | Surface ID for the games Fade effect. |
| `SURFACE_ID_ITEM_IMAGE`                |  `8`  | Surface ID for the Inventory items. |
| `SURFACE_ID_MAP`                       |  `9`  | Surface ID for the Map System. |
| `SURFACE_ID_SCREEN_GRAB`               | `10`  | Surface ID for the screenshot that is taken when entering inventory/related screens. |
| `SURFACE_ID_ARMS`                      | `11`  | Surface ID for the Weapons spritesheet. |
| `SURFACE_ID_ARMS_IMAGE`                | `12`  | Surface ID for the Weapon icons. |
| `SURFACE_ID_ROOM_NAME`                 | `13`  | Surface ID for the room name text. |
| `SURFACE_ID_STAGE_ITEM`                | `14`  | Surface ID for the teleporter warp icons. |
| `SURFACE_ID_LOADING`                   | `15`  | Surface ID for the 'LOADING' text that shows up on boot. |
| `SURFACE_ID_MY_CHAR`                   | `16`  | Surface ID for the Players spritesheet. |
| `SURFACE_ID_BULLET`                    | `17`  | Surface ID for the Bullets spritesheet. |
| `SURFACE_ID_CARET`                     | `19`  | Surface ID for the Carets spritesheet. |
| `SURFACE_ID_NPC_SYM`                   | `20`  | Surface ID for the 'NpcSym' spritesheet. |
| `SURFACE_ID_LEVEL_SPRITESET_1`         | `21`  | Surface ID for the current rooms "first" Npc spritesheet. |
| `SURFACE_ID_LEVEL_SPRITESET_2`         | `22`  | Surface ID for the current rooms "second" Npc spritesheet. |
| `SURFACE_ID_NPC_REGU`                  | `23`  | Surface ID for the 'NpcRegu' spritesheet. |
| `SURFACE_ID_TEXT_BOX`                  | `26`  | Surface ID for the TextBox and other Misc. sprites. |
| `SURFACE_ID_FACE`                      | `27`  | Surface ID for the Face spritesheets used in `<FAC`. |
| `SURFACE_ID_LEVEL_BACKGROUND`          | `28`  | Surface ID for the current rooms loaded background. |
| `SURFACE_ID_VALUE_VIEW`                | `29`  | Surface ID for the 'ValueView's that get drawn on screen. |
| `SURFACE_ID_TEXT_LINE1`                | `30`  | Surface ID used for the Tsc text drawing. |
| `SURFACE_ID_TEXT_LINE2`                | `31`  | Surface ID used for the Tsc text drawing. |
| `SURFACE_ID_TEXT_LINE3`                | `32`  | Surface ID used for the Tsc text drawing. |
| `SURFACE_ID_TEXT_LINE4`                | `33`  | Surface ID used for the Tsc text drawing. |
| `SURFACE_ID_TEXT_LINE5`                | `34`  | Surface ID used for the Tsc text drawing. |
| `SURFACE_ID_CREDIT_CAST`               | `35`  | Surface ID used for the Credits 'cast' being drawn on screen. |
| `SURFACE_ID_CREDITS_IMAGE`             | `36`  | Surface ID used for the Credits illustrations that appear on the side. |
| `SURFACE_ID_CASTS`                     | `37`  | Surface ID used for the Credits 'cast' spritesheet. |
| `TSC_BUFFER_SIZE`                      |`20480`| The amount of Bytes that a Tsc file can be loaded into (including Head.tsc)       |
| `WINDOW_WIDTH`                         | `320` | The games screen width, in original size rather than multiplied via currently set mode. |
| `WINDOW_HEIGHT`                        | `240` | The games screen height, in original size rather than multiplied via currently set mode. |
| `VS`                                   | `512` | Value the user may divide/multiply by in order to get world/screen coordinates.   |