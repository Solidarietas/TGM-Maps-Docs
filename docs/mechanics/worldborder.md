# World Border

This module is used to manage the vanilla Minecraft world border within the bounds of a PVP Arcade map. While only one border can be used at a time, the module lets you change the starting size, end size, delay, and center.

## Example

```json
	"border": {
		"startingSize": 1000,
		"endSize": 100,
		"center": "0, 60, 0",
		"delay": 20
	},
```

This example would see the worldborder start to go from 1000 blocks wide to 100 over the course of 20 seconds.

### World Border Attributes

| Attribute     | Description                                    | Value      |
|---------------|------------------------------------------------|------------|
| `startingSize`| The starting size in the length of one side.   | Number     |
| `endSize`     | The end size in the length of one side.        | Number     |
| `center`      | The central location of a world border.        | Coordinate |
| `delay`       | The delay in seconds until the border changes. | Number     |
