# Syntax

Flux map events are written as one event per line.
Events are typically split by a `|` (pipe) and into three portions in the following order;

1. Timestamp (in milliseconds)
2. Event type (see [Types](#Types))
3. Parameters (optional, leave as nothing to use default)

Example:  
`1000|GS|1x3`

# Types

**NOTE:** *Anywhere "time" is referenced in the table below, the unit is milliseconds*

| Type | Purpose | Parameters | Defaults |
| ---- | ------- | ---------- | -------- |
| `GS` | Changing the grid size | `WxH`, where `W` represents the width of the grid, and where `H` represents the height of the grid | `3x3` |
| `GT` | Setting the grid's translation | `X,Y`, where `X` is the x-coordinate to translate to and where `Y` is the y-coordinate to translate to | `0,0` |
| `CZ` | Setting the camera's zoom | `MODE,AMT` where `MODE` can be either `FOV`, `Z`, or `BOTH` and `AMT` represents the zoom intensity | `BOTH,0` |
| `CR` | Setting the camera's rotation | `A` where `A` is the Z angle of the camera in degrees | `0` |
| `FW` | White screen flash | `i,o`, where `i` is the time it takes for the flash to fade in and `o` is the time it takes to fade out | `0,1000` |
| `FB` | Black screen flash | `i,o`, where `i` is the time it takes for the flash to fade in and `o` is the time it takes to fade out | `0,1000` |