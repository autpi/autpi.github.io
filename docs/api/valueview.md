# ModCS.ValueView

The **ModCS.ValueView namespace** contains functions related to the ValueView functionality.

## ModCS.ValueView.Clear()

```lua
ModCS.ValueView.Clear()
```

Clears all ValueViews on screen.

## ModCS.ValueView.SetPlayer()

```lua
ModCS.ValueView.SetPlayer(num)
```

Puts a ValueView of number amount `num` at the Players position.

## ModCS.ValueView.SetNpc()

```lua
ModCS.ValueView.SetNpc(npc, num)
```

Puts a ValueView of number amount `num` at a [ModCS.Npc](/api/objects/npc/).

Sets the camera target to Game object `obj` (Can be [ModCS.Player](/api/objects/player/), a [ModCS.Npc](/api/objects/npc/), a [ModCS.Caret](/api/objects/caret/) or a [ModCS.Bullet](/api/objects/bullet/))

## ModCS.ValueView.SetCaret()

```lua
ModCS.ValueView.SetCaret(caret, num)
```

Puts a ValueView of number amount `num` at a [ModCS.Caret](/api/objects/caret/).

## ModCS.ValueView.SetBullet()

```lua
ModCS.ValueView.SetBullet(bullet, num)
```

Puts a ValueView of number amount `num` at a [ModCS.Bullet](/api/objects/bullet/).

## ModCS.ValueView.ActMain()

```lua
ModCS.ValueView.ActMain()
```

Runs the ValueView action code -- Should probably only be ran in a case where you're overwriting a game mode.

## ModCS.ValueView.DrawMain()

```lua
ModCS.ValueView.DrawMain(fx, fy)
```

Draws the ValueViews on screen at the camera position `fx` and `fy`, making it function for a new game mode the user may add.