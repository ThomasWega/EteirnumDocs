---
description: 'A typical Mob Area structure is as follows:'
---

# Structure

```json
{
  "medium1": {
    "name": "medium1",
    "world": "world",
    "box": {
      "min-x": 27.61,
      "min-y": 64.0,
      "min-z": -178.73,
      "max-x": 37.61,
      "max-y": 64.0,
      "max-z": -165.4
    },
    "spawn-interval-ticks": 20,
    "min-mobs": 1,
    "max-mobs": -1,
    "player-multiplier": 0.0,
    "mob-groups": [],
    "mob-names": []
  }
}
```

### Components

* **Name**: A unique name for the area. The `name` is used to reference the area within the game’s systems.
  * <mark style="color:orange;">The</mark> <mark style="color:orange;"></mark><mark style="color:orange;">`name`</mark> <mark style="color:orange;"></mark><mark style="color:orange;">must be unique across all areas to prevent conflicts.</mark>
  * It serves as the primary key for identifying the area in the game’s logic.
* **World**: A name of the world where the area is located
* **Box**: Specifies the boundaries of the area.&#x20;
  * Y axis is ignored in the calculations
* **Spawn Interval Ticks**: The frequency of mob spawns in ticks
* **Min Mobs**: Minimum amount of mobs to spawn on each spawn iteration
  * <mark style="color:orange;">Cannot be negative</mark>
* **Max Mobs:** Maximum amount of mobs to spawn on each spawn iteration
  * if `-1` no limit is applied
* **Player Multiplier**: Scales up the total amount of mobs spawned on each iteration based on the amount of players in the area
  * default is `0`
  * The formula is as follows: $$spawnAmount+(spawnAmount×playerCount×playerMultiplier)$$
* **Mob Groups**: Specifies the mob groups that spawn in the area. More info[ here](../mob-groups.md)
* **Mob Names**: Specifies the names of the mobs that spawn in the area
  * Doesn't include mob groups mob names
