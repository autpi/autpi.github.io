# ModCS.Back

The **ModCS.Back global object** represents the background for the stage loaded

ModCS.Back is userdata. You may access and edit the following values from it:

| Value        | Type                                 | Usage                                                        |
| ------------ | ------------------------------------ | ------------------------------------------------------------ |
| `width`     | Number (Casted to integer)            | The width of the background.                                 |
| `height`    | Number (Casted to integer)            | The height of the background.                                |
| `numX`      | Number (Casted to integer)            | Unused by vanilla game.                                      |
| `numY`      | Number (Casted to integer)            | Unused by vanilla game.                                      |
| `type`      | Number (Casted to integer)            | The type of background.                                      |
| `fx`        | Number (Casted to integer)            | Camera-related value, used for Ironhead and Clouds.          |
| `waterY`    | [Pixel Unit](/api/objects/pixel/)     | Global water level Y position.                               |



## ModCS.Back.Set()

```lua
ModCS.Back.Set("bkString", num)
```

Sets the stage background to the `bkString` file with the type `num`. This resets `ModCS.Back.waterY` to the vanilla value of 240 tiles down.

## ModCS.Back.ActMain()

```lua
ModCS.Back.ActMain()
```

Runs the Background action code -- Should probably only be ran in a case where you're overwriting a game mode.

## ModCS.Back.Put()

```lua
ModCS.Back.DrawMain(fx, fy)
```

Draws the background on screen at the camera position `fx` and `fy`, making it function for a new game mode the user may add.

## ModCS.Back.PutFront()

```lua
ModCS.Back.DrawFront(fx, fy)
```

Draws the foreground (for certain effects) on screen at the camera position `fx` and `fy`, making it function for a new game mode the user may add.