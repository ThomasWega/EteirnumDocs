---
description: Apply potion effect
---

# POTION

## Parameters:

* `potion`: The potion name. List [here](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/potion/PotionEffectType.html)
* `duration-ticks`: Duration of the potion
  * default is `200`
* `amplifier`: Level of the potion
  * default is `0`
* `ambient`: Whether the potion is ambient
  * makes potion effect produce more, translucent, particles
  * default is `false`
* `particles`: Whether this effect has particles or not
  * default is `true`
* `icon`: Whether this effect has an icon or not
  * default is `false`
* `extend`: Whether if the target already had the effect, it should just extend the duration
  * default is `false` (the current effect will be overridden)

Example:

```json5
"POTION": {
  "target": "TARGET",
  "potion": "blindness",
  "duration-ticks": 200,
  "amplifier": 1
}
```
