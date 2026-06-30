# ModCS.Npc

The **ModCS.Npc class** represents NPCs (Also known as Entities). NPCs are game objects used for enemies, cutscenes, enemy projectiles and (some) bosses. Examples are Toroko, First Cave Critter, Puu Black, etc.

A ModCS.Npc is userdata. You may access and edit the following values from it:

| Value           | Type                                 | Usage                                                        |
| --------------- | ------------------------------------ | ------------------------------------------------------------ |
| `x`             | [Pixel Unit](/api/objects/pixel/)    | X position of the NPC.                                       |
| `y`             | [Pixel Unit](/api/objects/pixel/)    | Y position of the NPC.                                       |
| `xm`            | [Pixel Unit](/api/objects/pixel/)    | X velocity of the NPC. This value does nothing by itself, but can be used with [ModCS.Npc.Move()](/api/objects/npc/functions/#modcsnpcmove). |
| `ym`            | [Pixel Unit](/api/objects/pixel/)    | Y velocity of the NPC. This value does nothing by itself, but can be used with [ModCS.Npc.Move()](/api/objects/npc/functions/#modcsnpcmove). |
| `xm2`           | [Pixel Unit](/api/objects/pixel/)    | Alternative X velocity of the NPC. This value does nothing by itself, but can be used with [ModCS.Npc.Move2()](/api/objects/npc/functions/#modcsnpcmove2). |
| `ym2`         | [Pixel Unit](/api/objects/pixel/)    | Alternative Y velocity of the NPC. This value does nothing by itself, but can be used with [ModCS.Npc.Move2()](/api/objects/npc/functions/#modcsnpcmove2). |
| `tgt_x`    | [Pixel Unit](/api/objects/pixel/)    | Target X value. This variable does nothing by itself. |
| `tgt_y`   | [Pixel Unit](/api/objects/pixel/)    | Target Y value. This variable does nothing by itself. |
| `id`            | [NPC Type ID](/api/objects/npc/id/)    | ID of the NPC.                                               |
| `flag`          | [Flag](/api/flags/flag/) | Flag of the NPC.                                             |
| `event`         | [Event](/api/tsc/#events)            | [TSC Event](/api/tsc/#events) of the NPC.                    |
| `surf`          | [Surface](/api/drawing/surface/)     | The surface that the NPC will draw from.                     |
| `hit_voice`     | [Sound ID](/api/sound/sound/#sound-effects-id-reference) | The sound effect that will play when the NPC gets hit.       |
| `destroy_voice` | [Sound ID](/api/sound/sound/#sound-effects-id-reference) | The sound effect that will play when the NPC dies.           |
| `life`          | Number (Casted to integer)           | The health points of the NPC.                                |
| `damage`        | Number (Casted to integer)           | The amount of damage the NPC deals to the player upon touching. |
| `exp`           | Number (Casted to integer)           | The XP worth of the NPC.                                     |
| `smoke_size`    | Number (Casted to integer)           | The amount of smoke the NPC will spawn after dying. Can be from 0 to 3 (0 being no smoke being spawned upon death). |
| `direct`        | [Direction](/api/objects/direction/) | Direction of the NPC.                                        |
| `ani_no`        | Number (Casted to integer)           | Animation frame value. This variable does nothing by itself, but can be used to switch between animation frames. |
| `ani_wait`      | Number (Casted to integer)           | Animation timer value. This variable does nothing by itself, but can be used as a timer between animation frames. |
| `act_no`        | Number (Casted to integer)           | Act state value. This variable does nothing by itself, but can be changed with the `<ANP` TSC command. |
| `act_wait`      | Number (Casted to integer)           | Act state timer value. This variable does nothing by itself, but can be used as a timer between act states. |
| `count1`   | Number (Casted to integer)           | Counter value. This variable does nothing by itself. |
| `count2` | Number (Casted to integer)           | Counter value. This variable does nothing by itself. |
| `pNpc`          | [NPC](/api/objects/npc/)             | Parent NPC value.                                            |
| `tgt_mc`        | [Player](/api/objects/player/)       | Functions the same as ModCS.Player in Freeware AutPI, but can be used in other engines for multiplayer ports. In other engines, this would be the nearest player. |
| `x_cs`             | Number (Casted to integer)    | X position of the NPC. (Multiplied by 512, the original Cave Story style.)                                       |
| `y_cs`             | Number (Casted to integer)    | Y position of the NPC. (Multiplied by 512, the original Cave Story style.)                                       |
| `xm_cs`            | Number (Casted to integer)    | X velocity of the NPC. (Multiplied by 512, the original Cave Story style.) |
| `ym_cs`            | Number (Casted to integer)    | Y velocity of the NPC. (Multiplied by 512, the original Cave Story style.) |
| `xm2_cs`           | Number (Casted to integer)    | Alternative X velocity of the NPC. (Multiplied by 512, the original Cave Story style.) |
| `ym2_cs`         | Number (Casted to integer)    | (Multiplied by 512, the original Cave Story style.) |
| `tgt_x_cs`    | Number (Casted to integer)    | Target X value. (Multiplied by 512, the original Cave Story style.) This variable does nothing by itself. |
| `tgt_y_cs`   | Number (Casted to integer)    | Target Y value. (Multiplied by 512, the original Cave Story style.) This variable does nothing by itself. |

## The NPC Buffer
Spawned NPCs in Cave Story are stored in a buffer (or list) of 512 entries. Although the NPC buffer size is 512, the game starts spawning NPCs at different positions in the buffer in different places. Examples include:

- NPCs loaded from a PXE file start from 170.

- NPCs spawned by `<SNP` start from 256.

- Water splash entities start from 0.

When the game spawns NPCs it checks trough the NPC buffer and finds a spot that's not currently occupied by an alive NPC and replaces that spot with the NPC it's spawning. When the NPC in that spot dies, the spot is freed out for when the game decides to spawn another NPC again.

!!! Warning
	If you will be using any of the following functions for actively updating an NPC you will have to actively retrieve the NPC as well.

## ModCS.Npc.GetByEvent()

```lua
ModCS.Npc.GetByEvent(event, ignorealive)
```

Searches the current buffer of spawned NPCs for one with an [Event](/api/tsc/#events) number `event` and returns a ModCS.Npc of that NPC. Returns a nil otherwise. `ignorealive` is an optional boolean, that if true, will return an npc even if the npc is not alive/does not exist.

## ModCS.Npc.GetByFlag()

```lua
ModCS.Npc.GetByFlag(flag, ignorealive)
```

Searches the current buffer of spawned NPCs for one with an [Flag](/api/flags/flag/) number `flag` and returns a ModCS.Npc of that NPC. Returns a nil otherwise. `ignorealive` is an optional boolean, that if true, will return an npc even if the npc is not alive/does not exist.

## ModCS.Npc.GetByID()

```lua
ModCS.Npc.GetByID(id, ignorealive)
```

Searches the current buffer of spawned NPCs for one with an [NPC Type ID](/api/objects/npc/id/) number `id` and returns a ModCS.Npc of that NPC. Returns a nil otherwise. `ignorealive` is an optional boolean, that if true, will return an npc even if the npc is not alive/does not exist.

## ModCS.Npc.GetByBufferIndex()

```lua
ModCS.Npc.GetByBufferIndex(index, ignorealive)
```

Directly gets `index` NPC from the NPC buffer. `ignorealive` is an optional boolean, that if true, will return an npc even if the npc is not alive/does not exist.

## ModCS.Npc.Spawn()

```lua
ModCS.Npc.Spawn(npctype, x, y, start_index)
```

Spawns an NPC of [NPC Type](/api/objects/npc/id/) `npctype` on [Pixel Unit](/api/objects/pixel/) coordinates `x` and `y`. If `start_index` is specified the NPC buffer start position for the NPC summon will be `start_index`. Otherwise the NPC buffer start position will be 256.

Returns a ModCS.Npc of the spawned NPC. 

## ModCS.Npc.Spawn2()

```lua
ModCS.Npc.Spawn2(npctype, x, y, xm, ym, direction, start_index)
```

Spawns an NPC of [NPC Type](/api/objects/npc/id/) `npctype` on [Pixel Unit](/api/objects/pixel/) coordinates `x` and `y`, with `xm`, `ym`, and `direction` specified. If `start_index` is specified the NPC buffer start position for the NPC summon will be `start_index`. Otherwise the NPC buffer start position will be 256.

Returns a ModCS.Npc of the spawned NPC. 

## ModCS.Npc.Spawn3()

```lua
ModCS.Npc.Spawn3(npctype, x, y, xm, ym, direction, parentNpc, start_index)
```

Spawns an NPC of [NPC Type](/api/objects/npc/id/) `npctype` on [Pixel Unit](/api/objects/pixel/) coordinates `x` and `y`, with `xm`, `ym`, and `direction` specified, with a "parent" (`parentNpc`), usually being the current entity. If `start_index` is specified the NPC buffer start position for the NPC summon will be `start_index`. Otherwise the NPC buffer start position will be 256.

Returns a ModCS.Npc of the spawned NPC. 

## ModCS.Npc.Explode()

```lua
ModCS.Npc.Explode(x, y, offset, amount, dir)
```

Create a massive explosion of `amount` smoke at coordinates `x` and `y`, with `offset` from X:Y randomly set. `dir` is an optional parameter. If `dir` is set to `1`, the smoke will spawn with the up facing direction instead. Any other `dir` given will be interpreted as `0`.

## ModCS.Npc.SpawnExp()

```lua
ModCS.Npc.SpawnExp(x, y, amount)
```

Spawns exp/heart/missile pickup objects at coordinates `x` and `y` with `amount` given.

## ModCS.Npc.GetSuperX()

```lua
ModCS.Npc.GetSuperX()
```

Returns the "Super" X position -- a variable npcs use in Cave Story to have multiple npcs focus on the same point via a global variable.

## ModCS.Npc.GetSuperY()

```lua
ModCS.Npc.GetSuperY()
```

Returns the "Super" Y position -- a variable npcs use in Cave Story to have multiple npcs focus on the same point via a global variable.

## ModCS.Npc.SetSuperX()

```lua
ModCS.Npc.SetSuperX(value)
```

Sets the "Super" X position to `value`. The value is a [Pixel Unit](/api/objects/pixel/)!

## ModCS.Npc.SetSuperY()

```lua
ModCS.Npc.SetSuperY(value)
```

Sets the "Super" Y position to `value`. The value is a [Pixel Unit](/api/objects/pixel/)!

## ModCS.Npc.GetCurlyShootX()

```lua
ModCS.Npc.GetCurlyShootX()
```

Returns the "NPC Curly Shoot" X position -- a variable the curly gun npc uses to decide where to shoot her weapon.

## ModCS.Npc.GetCurlyShootY()

```lua
ModCS.Npc.GetCurlyShootY()
```

Returns the "NPC Curly Shoot" Y position -- a variable the curly gun npc uses to decide where to shoot her weapon.

## ModCS.Npc.SetCurlyShootX()

```lua
ModCS.Npc.SetCurlyShootX(value)
```

Sets the "NPC Curly Shoot" X position to `value`. The value is a [Pixel Unit](/api/objects/pixel/)!

## ModCS.Npc.SetCurlyShootY()

```lua
ModCS.Npc.SetCurlyShootY(value)
```

Sets the "NPC Curly Shoot" Y position to `value`. The value is a [Pixel Unit](/api/objects/pixel/)!

## ModCS.Npc.GetCurlyShootWait()

```lua
ModCS.Npc.GetCurlyShootWait()
```

Returns the "NPC Curly Shoot" wait timer.

## ModCS.Npc.SetCurlyShootWait()

```lua
ModCS.Npc.SetCurlyShootWait(value)
```

Sets the "NPC Curly Shoot" wait timer to `value`.


## ModCS.Npc.Init()

```lua
ModCS.Npc.Init()
```

Resets all Npcs, like done when starting a new save.

## ModCS.Npc.ActMain()

```lua
ModCS.Npc.ActMain()
```

Runs all of the Npc action code -- Should probably only be ran in a case where you're overwriting a game mode.

## ModCS.Npc.TileHitCode()

```lua
ModCS.Npc.TileHitCode()
```

Runs the code for npcs collision against tiles -- Should probably only be ran in a case where you're overwriting a game mode.

## ModCS.Npc.DrawMain()

```lua
ModCS.Npc.DrawMain(fx, fy)
```

Draws the npcs on screen at the camera position `fx` and `fy`, making it function for a new game mode the user may add.