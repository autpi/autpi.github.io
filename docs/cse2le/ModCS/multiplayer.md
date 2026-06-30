# ModCS.Multiplayer

This contains multiple functions pertaining to multiplayer functionality. Technically, this also contains clones of all of the `ModCS.Player` functions, except there's an extra argument at the start for `player`.

## ModCS.Multiplayer.GetPlayerCount()

```lua
ModCS.Multiplayer.GetPlayerCount()
```

Returns the amount of players currently playing the game, whether alive or dead.

## ModCS.GetMaxPlayerCount()

```lua
ModCS.Multiplayer.GetMaxPlayerCount()
```

Returns the maximum amount of players allowed to play the game.

## ModCS.Multiplayer.GetByID()

```lua
ModCS.Multiplayer.GetByID(id)
```

Returns a `ModCS.Multiplayer` (basically a `ModCS.Player`) of the player `id`. `id` can be anywhere between 1-8.
Keep in mind how many players are enabled in `mods.ini`. The recommended is 2 or 4. The maximum is 8.

## ModCS.Multiplayer.IsPlaying()

```lua
ModCS.Multiplayer.IsPlaying(player)
```

Returns true if `player` is currently playing the game.

## ModCS.Multiplayer.IsAlive()

```lua
ModCS.Multiplayer.IsAlive(player)
```

Returns true if `player` is alive.

## ModCS.Multiplayer.IsDead()

```lua
ModCS.Multiplayer.IsDead(player)
```

Returns true if `player` is dead.

## ModCS.Multiplayer.ValueView()

```lua
ModCS.Multiplayer.ValueView(player, value)
```

Spawns a ValueView with `value` at the `player` x/y position.