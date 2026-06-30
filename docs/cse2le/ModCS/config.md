# ModCS.Config (CSE2LE)

The **ModCS.Config class** represents the Config that CSE2LE uses.

A ModCS.Config is userdata. You may access and edit the following values from it:

| Value           | Type                                 | Usage                                                        |
| --------------- | ------------------------------------ | ------------------------------------------------------------ |
| `60fps`         | Boolean                              | If this is true, the game will boot in 60fps (Assuming force 50fps isn't enabled) |
| `smooth_scrolling` | Boolean                           | If this is true, the game will scroll the camera more smoothly in resolutions higher than the base resolution (Assuming `Enhanced Scrolling` is disabled) |
| `integer_scaling` | Boolean (Saves to res.dat)         | If this is true, the game will Integer Scale its window if resized. |
| `display_mode`   | Number (Casted to integer, saves to res.dat) | Window size. Set to 0 for fullscreen. |
| `exp_shared`     | Boolean (Saves to Config.MP.dat) | Multiplayer toggle for Experience being shared when picked up. |
| `life_shared` | Boolean (Saves to Config.MP.dat) | Multiplayer toggle for Health pickups being shared when grabbed. |
| `ammo_shared` | Boolean (Saves to Config.MP.dat) | Multiplayer toggle for Missile pickups being shared when grabbed. |
| `deathlink` | Boolean (Saves to Config.MP.dat) | Multiplayer toggle for doing a game over when only 1 player dies. |
| `boss_hp_scaling` | Boolean (Saves to Config.MP.dat) | Multiplayer toggle for boss HP scaling with amount of players. |
| `keyboard_player_id` | Number (Casted to integer)      | Which player ID the keyboard user is if multiplayer is enabled. Can be a value between 1-8. (The game will interpret it as 0-7, but lua will use 1-8 automatically.) |
| `controller_a_player_id` | Number (Casted to integer)  | Which player ID the first controller user is if multiplayer is enabled. Can be a value between 1-8. (The game will interpret it as 0-7, but lua will use 1-8 automatically.) |
| `controller_b_player_id` | Number (Casted to integer)  | Which player ID the second controller user is if multiplayer is enabled. Can be a value between 1-8. (The game will interpret it as 0-7, but lua will use 1-8 automatically.) |
| `controller_c_player_id` | Number (Casted to integer)  | Which player ID the third controller user is if multiplayer is enabled. Can be a value between 1-8. (The game will interpret it as 0-7, but lua will use 1-8 automatically.) |
| `controller_d_player_id` | Number (Casted to integer)  | Which player ID the fourth controller user is if multiplayer is enabled. Can be a value between 1-8. (The game will interpret it as 0-7, but lua will use 1-8 automatically.) |
| `controller_e_player_id` | Number (Casted to integer)  | Which player ID the fifth controller user is if multiplayer is enabled. Can be a value between 1-8. (The game will interpret it as 0-7, but lua will use 1-8 automatically.) |
| `controller_f_player_id` | Number (Casted to integer)  | Which player ID the sixth controller user is if multiplayer is enabled. Can be a value between 1-8. (The game will interpret it as 0-7, but lua will use 1-8 automatically.) |
| `controller_g_player_id` | Number (Casted to integer)  | Which player ID the seventh controller user is if multiplayer is enabled. Can be a value between 1-8. (The game will interpret it as 0-7, but lua will use 1-8 automatically.) |
| `controller_h_player_id` | Number (Casted to integer)  | Which player ID the eighth controller user is if multiplayer is enabled. Can be a value between 1-8. (The game will interpret it as 0-7, but lua will use 1-8 automatically.) |
| `conf.bindings.up.TYPE` | Number (Casted to integer) | What button "up" is bound to. TYPE should be `keyboard`, or `controller_a`, `controller_b`, etc. up to `controller_h`. |
| `conf.bindings.down.TYPE` | Number (Casted to integer) | What button "down" is bound to. TYPE should be `keyboard`, or `controller_a`, `controller_b`, etc. up to `controller_h`. |
| `conf.bindings.left.TYPE` | Number (Casted to integer) | What button "left" is bound to. TYPE should be `keyboard`, or `controller_a`, `controller_b`, etc. up to `controller_h`. |
| `conf.bindings.right.TYPE` | Number (Casted to integer) | What button "right" is bound to. TYPE should be `keyboard`, or `controller_a`, `controller_b`, etc. up to `controller_h`. |
| `conf.bindings.alt_up.TYPE` | Number (Casted to integer) | What button "alternate up" is bound to. TYPE should be `keyboard`, or `controller_a`, `controller_b`, etc. up to `controller_h`. |
| `conf.bindings.alt_down.TYPE` | Number (Casted to integer) | What button "alternate down" is bound to. TYPE should be `keyboard`, or `controller_a`, `controller_b`, etc. up to `controller_h`. |
| `conf.bindings.alt_left.TYPE` | Number (Casted to integer) | What button "alternate left" is bound to. TYPE should be `keyboard`, or `controller_a`, `controller_b`, etc. up to `controller_h`. |
| `conf.bindings.alt_right.TYPE` | Number (Casted to integer) | What button "alternate right" is bound to. TYPE should be `keyboard`, or `controller_a`, `controller_b`, etc. up to `controller_h`. |
| `conf.bindings.ok.TYPE` | Number (Casted to integer) | What button "ok" is bound to. TYPE should be `keyboard`, or `controller_a`, `controller_b`, etc. up to `controller_h`. |
| `conf.bindings.cancel.TYPE` | Number (Casted to integer) | What button "cancel" is bound to. TYPE should be `keyboard`, or `controller_a`, `controller_b`, etc. up to `controller_h`. |
| `conf.bindings.jump.TYPE` | Number (Casted to integer) | What button "jump" is bound to. TYPE should be `keyboard`, or `controller_a`, `controller_b`, etc. up to `controller_h`. |
| `conf.bindings.shoot.TYPE` | Number (Casted to integer) | What button "shoot" is bound to. TYPE should be `keyboard`, or `controller_a`, `controller_b`, etc. up to `controller_h`. |
| `conf.bindings.armsrev.TYPE` | Number (Casted to integer) | What button "arms reverse" is bound to. TYPE should be `keyboard`, or `controller_a`, `controller_b`, etc. up to `controller_h`. |
| `conf.bindings.arms.TYPE` | Number (Casted to integer) | What button "arms" is bound to. TYPE should be `keyboard`, or `controller_a`, `controller_b`, etc. up to `controller_h`. |
| `conf.bindings.item.TYPE` | Number (Casted to integer) | What button "item" is bound to. TYPE should be `keyboard`, or `controller_a`, `controller_b`, etc. up to `controller_h`. |
| `conf.bindings.map.TYPE` | Number (Casted to integer) | What button "map" is bound to. TYPE should be `keyboard`, or `controller_a`, `controller_b`, etc. up to `controller_h`. |
| `conf.bindings.shift.TYPE` | Number (Casted to integer) | What button "shift" is bound to. TYPE should be `keyboard`, or `controller_a`, `controller_b`, etc. up to `controller_h`. |
| `conf.bindings.pause.TYPE` | Number (Casted to integer) | What button "pause" is bound to. TYPE should be `keyboard`, or `controller_a`, `controller_b`, etc. up to `controller_h`. |

## ModCS.Config.Get()

```lua
ModCS.Config.Get()
```

Returns a `ModCS.Config` by loading the config files if they exist, or populating them with defaults otherwise. You may use this to edit the config as you wish.

## ModCS.Config.Apply()

```lua
ModCS.Config.Apply(cfg)
```

Applies `cfg` to the game, making some things be set in real time (bindings, integer scaling, etc.)

## ModCS.Config.Save()

```lua
ModCS.Config.Save(cfg)
```

Saves a `ModCS.Config` to the correct config files. This will also run `ModCS.Config.Apply(cfg)` automatically.