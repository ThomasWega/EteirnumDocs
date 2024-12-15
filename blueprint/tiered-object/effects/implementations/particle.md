---
description: Creates a particle effect
---

# PARTICLE

## **Parameters**:

* `particle-data`: All data for the particle
  * `particle`: The type of particle (e.g., `EXPLOSION`, `HEART`). List [here](https://github.com/Fierioziy/ParticleNativeAPI/blob/master/ParticleNativeAPI-api/src/main/java/com/github/fierioziy/particlenativeapi/api/particle/ParticleList_1_13.java)
  * `count`: Number of particles
    * default is `1`
  * `x`: The offset for the X location
    * default is `0.0`
  * `y`: The offset for the Y location
    * default is `0.0`
  * `z`: The offset for the Z location
    * default is `0.0`
  * `red`: The red color. Used for example for `DUST` particle
    * from `0` to `255`
  * `green`: The green color. Used for example for `DUST` particle
    * from `0` to `255`
  * `blue`: The blue color. Used for example for `DUST` particle
    * from `0` to `255`
  * `red-fade`: The fade color of red. Used for example for `DUST_COLOR_TRANSITION`
    * from `0` to `255`
  * `green-fade`: The fade color of green. Used for example for `DUST_COLOR_TRANSITION`
    * from `0` to `255`
  * `blue-fade`: The fade color of blue. Used for example for `DUST_COLOR_TRANSITION`
    * from `0` to `255`
  * `size`: Size of the particle. Used for example for `DUST` particle
    * default is `1`
  * `speed`: Speed of the particle
    * default is `1`
  * `direction-x`: The X direction (motion) the particle. Used for example for `BLOCK_CRACK`
    * default is `0`
  * `direction-y`: The Y direction (motion) the particle. Used for example for `BLOCK_CRACK`
    * default is `0`
  * `direction-z`: The Z direction (motion) the particle. Used for example for `BLOCK_CRACK`
    * default is `0`
  * `material`: Material of the particle block/item. Used for example for `BLOCK_CRACK`
    * default is `STONE`
      * should be in `UPPER_CASE`
  * `roll-angle`: Rotation of the particle. Used for example for `SCULK_CHARGE`
    * default is `0`
  * `shriek-delay-ticks`: Delay of `SHRIEK` particle
    * default is `0`

{% hint style="success" %}
[Viewers parameter](../#viewable-effects) supported
{% endhint %}

Example:

```json
"PARTICLE": {
  "propagate": true,
  "target": "LOCATION",
  "viewers": "ALL",
  "particle-data": {
    "particle": "LAVA"
  }
}
```
