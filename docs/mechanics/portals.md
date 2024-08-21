# Portals

This module is used to teleport players to different parts of the map.

## Example 1

```json
    "portals": [ 
        {"from": "blue-portal", "to": "10, 23, 34, 180", "teams": ["blue"], "sound": false}
    ],
```

## Example 2

```json
    "portals": [ 
        {"from": "blue-portal", "to": "10, 23, 34, 180", "teams": ["blue"], "sound": false}
    ],
```

### Portal Attributes

| Attribute | Description                                                         | Value      |
|-----------|---------------------------------------------------------------------|------------|
| `from`    | The location in which the player must enter from.                   | Region     |
| `to`      | The location in which the player is teleported to.                  | Coordinate |
| `teams`   | The teams that are allowed to enter through this portal.            | String     |
| `sound`   | Whether or not the default "zip" sound should be played upon entry. | Boolean    |
| `flags`   | Contains portal attributes that define teleport behaviour.          | Parent     |

<span class="label label-note">Note</span> A region is required to define `from`. Portals are also automatically enabled for spectators.

### Portal Teleport Flags
| Flag                    | Description                                                                                 | Value   | Default |
|-------------------------|---------------------------------------------------------------------------------------------|---------|---------|
| `relative-x-position`   | Whether to teleport the target relative to their current location on the x-axis.            | Boolean | `false` |
| `relative-y-position`   | Whether to teleport the target relative to their current location on the y-axis.            | Boolean | `false` |
| `relative-z-position`   | Whether to teleport the target relative to their current location on the z-axis.            | Boolean | `false` |
| `relative-x-velocity`   | Whether to maintain the player's relative velocity on the x-axis during teleportation.      | Boolean | `true`  |
| `relative-y-velocity`   | Whether to maintain the player's relative velocity on the y-axis during teleportation.      | Boolean | `true`  |
| `relative-z-velocity`   | Whether to maintain the player's relative velocity on the z-axis during teleportation.      | Boolean | `true`  |
| `relative-yaw`          | Whether to maintain the relative yaw (horizontal rotation) during teleportation.            | Boolean | `true`  |
| `relative-pitch`        | Whether to maintain the relative pitch (vertical rotation) during teleportation.            | Boolean | `true`  |
| `retain-passengers`     | Indicates whether the entity's passengers should be retained during teleportation.          | Boolean | `true`  |
| `retain-vehicle`        | Indicates whether the entity should remain mounted on a vehicle during teleportation.       | Boolean | `true`  |
| `retain-open-inventory` | Indicates whether the player should keep their current open inventory during teleportation. | Boolean | `true`  |

### Additional Context:
- **Relative Velocity Flags** (`relative-x-velocity`, `relative-y-velocity`, `relative-z-velocity`):
    - These flags currently only work on players, though work is being done to make them work on all entities. 

- **Retain Flags** (`retain-passengers`, `retain-vehicle`, `retain-open-inventory`):
    - **RETAIN_PASSENGERS**: If set to `true`, the entity's passengers are not required to be removed before teleportation. However, if teleporting to a different world with this flag enabled while the entity has passengers, the teleportation will fail.
    - **RETAIN_VEHICLE**: If set to `true`, the entity will remain mounted on a vehicle during teleportation. However, if teleporting to a different world with this flag enabled while the entity is riding another entity, the teleportation will fail.
    - **RETAIN_OPEN_INVENTORY**: If set to `true`, the player's open inventory will not be closed during teleportation. This flag is ignored when teleporting to a different world.
