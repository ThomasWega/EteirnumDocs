---
description: Remove a potion effect from the target
---

# REMOVE\_POTION

## Parameters:

* `potion`: The potion name. List [here](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/potion/PotionEffectType.html)

Example: (Remove all negative potion effects)

```json
"effects": [
  {
    "REMOVE_POTION": [
      {
        "ignore-unapply": true,
        "potion": "UNLUCK"
      },
      {
        "ignore-unapply": true,
        "potion": "BAD_OMEN"
      },
      {
        "ignore-unapply": true,
        "potion": "BLINDNESS"
      },
      {
        "ignore-unapply": true,
        "potion": "GLOWING"
      },
      {
        "ignore-unapply": true,
        "potion": "HUNGER"
      },
      {
        "ignore-unapply": true,
        "potion": "INSTANT_DAMAGE"
      },
      {
        "ignore-unapply": true,
        "potion": "LEVITATION"
      },
      {
        "ignore-unapply": true,
        "potion": "MINING_FATIGUE"
      },
      {
        "ignore-unapply": true,
        "potion": "NAUSEA"
      },
      {
        "ignore-unapply": true,
        "potion": "POISON"
      },
      {
        "ignore-unapply": true,
        "potion": "SLOWNESS"
      },
      {
        "ignore-unapply": true,
        "potion": "WEAKNESS"
      },
      {
        "ignore-unapply": true,
        "potion": "WITHER"
      }
    ]
  }
]
```
