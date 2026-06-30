# ModCS.Map

The **ModCS.Map namespace** contains functions related to Maps.

Maps are a collection of files stored in the `/data/Stage/` folder. They are only usuable in-game via a [Stage](/api/stage/).

Maps are composed of 3 types of files:

- PXM (PixMap) files - For storing tile placement.

- PXE (PixEvent or PixEntity) - For storing NPC placement.

- TSC Files - For storing an individual map's [TextScript](/api/tsc/).

## Tile Unit

Map files (TSC included) use **Tile Units** for coordinates rather than [Pixel Units](/api/objects/pixel/). One Tile Unit is 16x16 Pixel Units.

## ModCS.Map.GetWidth()

```lua
ModCS.Map.GetWidth()
```

Returns the width in tile units of the current loaded map.

## ModCS.Map.GetHeight()

```lua
ModCS.Map.GetHeight()
```

Returns the height in tile units of the current loaded map.

## ModCS.Map.GetAttribute()

```lua
ModCS.Map.GetAttribute(x, y)
```

Returns the attribute of the tile at tile unit coordinates `x` and `y`.

## ModCS.Map.GetTile()

```lua
ModCS.Map.GetTile(x, y)
```

Returns the tile ID at tile unit coordinates `x` and `y`.

## ModCS.Map.ChangeTile()

```lua
ModCS.Map.ChangeTile(no, x, y)
```

Changes the tile at tile unit coordinates `x` and `y` of the current map to tile `no`.

## ModCS.Map.ShiftTile()

```lua
ModCS.Map.ShiftTile(x, y)
```

"Shifts" the tile at tile unit coordinates `x` and `y` 1 tile ID to the left in its tileset. This is what "Snack" blocks do when destroyed.

## ModCS.Map.DeleteTile()

```lua
ModCS.Map.DeleteTile(x, y)
```

Deletes the tile at tile unit coordinates `x` and `y`.

## ModCS.Map.PutName()

```lua
ModCS.Map.PutName(mini)
```

Draws the current room name on screen. `mini` is an optional Boolean, if true, the map name will render like it does in the Map System, rather than a `<MNA` style.