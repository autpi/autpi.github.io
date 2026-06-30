# NPC Bits

**NPC Bits** (Also known as NPC Flags) are toggles on NPCs that enable certain NPC features. They can be turned on for individual [NPC Types](/api/objects/npc/id/) as well as for individual NPCs in a PXE file.

!!! Note
	In the original game NPC Bits are bit-wise. Because of this, many editors show bitwise information for them. For simplicity's sake ModCS uses normal decimal values.

| Value | Bitwise Value | Const Name | Usage                                                        |
| ----- | ------------- | ---------- | ------------------------------------------------------------ |
| 0     | 0x0001        |`NPC_SOLID_SOFT`| Collision against player - Pushes player out.                |
| 1     | 0x0002        |`NPC_IGNORE_TILE_44`| Ignore tile attribute 44.                                    |
| 2     | 0x0004        |`NPC_INVULNERABLE`| Cannot be hurt and has a different hit effect when hit by a bullet. |
| 3     | 0x0008        |`NPC_IGNORE_SOLIDITY`| Ignore tile collision.                                       |
| 4     | 0x0010        |`NPC_BOUNCY`| The top of the NPC is bouncy.                                |
| 5     | 0x0020        |`NPC_SHOOTABLE`| The NPC is shootable.                                        |
| 6     | 0x0040        |`NPC_SOLID_HARD`| Collision against player.                                    |
| 7     | 0x0080        |`NPC_REAR_AND_TOP_DONT_HURT`| Rear and top of the NPC does not hurt the player.            |
| 8     | 0x0100        |`NPC_EVENT_WHEN_TOUCHED`| The [TSC Event](/api/tsc/#events) specified in the `event` parameter of the ModCS.Npc will run when the player touches the NPC. |
| 9     | 0x0200        |`NPC_EVENT_WHEN_KILLED`| The [TSC Event](/api/tsc/#events) specified in the `event` parameter of the ModCS.Npc will run when the NPC dies. |
| 11    | 0x0800        |`NPC_APPEAR_WHEN_FLAG_SET`| The NPC will not spawn unless the [Flag](/api/flags/flag/) specified in the `flag` parameter of ModCS.Npc is set. |
| 12    | 0x1000        |`NPC_SPAWN_IN_OTHER_DIRECTION`| The NPC will spawn with the `direct` parameter of the ModCS.Npc being set to 2. |
| 13    | 0x2000        |`NPC_INTERACTABLE`| If the player interacts with the NPC the [TSC Event](/api/tsc/#events) specified in the `event` parameter of the ModCS.Npc will run. |
| 14    | 0x4000        |`NPC_HIDE_WHEN_FLAG_SET`| The NPC will not spawn if the [Flag](/api/flags/flag/) specified in the `flag` parameter of ModCS.Npc is set. |
| 15    | 0x8000        |`NPC_SHOW_DAMAGE`| Damage dealt to the NPC will show in a damage indicator.     |

## ModCS.Npc.SetBit()

```lua
ModCS.Npc.SetBit(npc, bit)
```

Sets the bit `bit` for `npc`.

## ModCS.Npc.UnsetBit()

```lua
ModCS.Npc.UnsetBit(npc, bit)
```

Unsets the bit `bit` for `npc`.

## ModCS.Npc.CheckBit()

```lua
ModCS.Npc.CheckBit(npc, bit)
```

Returns true if the bit `bit` for `npc` is set. Returns false otherwise.