# Legacy (1.8) Features

This module is used to enable legacy features on a map. 

## Example 1

Makes map use 1.8 spam-clicking and weapon damage values, but do not restore 1.8 armor behaviour (infinite armor toughness)

```json
	"legacy": {
		"attack-speed": true,
		"damage": true,
		"armor": false
	},
```

## Example 2

Make the map use 1.8 health regeneration and saturation behaviour.

```json
	"legacy": {
		"regen": true
	},
```

### Countdown Structure
| Field          | Description                                                                                                                   | Type    | Required | Default |
|----------------|-------------------------------------------------------------------------------------------------------------------------------|---------|----------|---------|
| `attack-speed` | Whether the map should use spam clicking, legacy (1.8), weapon attack speed behaviour.                                        | Boolean | No       | False   |
| `damage`       | Whether to use legacy damage values on weapons. Axes will do 1 less damage than their respective swords.                      | Boolean | No       | False   |
| `armor`        | Whether to use legacy armor damage calculations. In short, armor toughness is considered to be infinite for all armors.       | Boolean | No       | False   |
| `shield`       | Whether to enable legacy blocking/shield behaviour. Instead of blocking attacks shields will reduce damage by 50% by default. | Boolean | No       | False   |
| `regen`        | Whether to use legacy (1.8) player health regeneration and saturation mechanics.                                              | Boolean | No       | False   |

Per-map legacy knockback, custom knockback, and shield damage reduction settings are actively in development. They can currently only be set in the global TGM config.