---
description: Creates a sphere made out of particles
---

# PARTICLE\_SPHERE

## Parameters:

* All [Parameters of `PARTICLE` effect](particle.md#parameters)
* `particles`: The number of particles forming the sphere
  * default is `1`
  * used only if `fill` is `false`
* `density`: The density of the particles
  * default is `0.4`
  * used only if `fill` is `true`
* `fill`: Toggle whether to fully fill in the sphere with particles
  * default is `false`

Example:

```json
"PARTICLE_SPHERE": {
  "target": "INVOKER",
  "radius": 1,
  "particles": 100,
  "particle-data": {
    "particle": "GLOW",
    "y": 1
  }
}
```
