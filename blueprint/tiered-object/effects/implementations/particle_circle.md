---
description: Creates a circle made out of particles
---

# PARTICLE\_CIRCLE

## Parameters:

* All [Parameters of `PARTICLE` effect](particle.md#parameters)
* `particles`: The number of particles forming the circle
  * default is `1`
  * used only if `fill` is `false`
* `density`: The density of the particles
  * default is `0.4`
  * used only if `fill` is `true`
* `fill`: Toggle whether to fill in the circle with particles
  * default is `false`
* `rotation-x`: Rotate the circle in an angle on X axis
  * default is `0`
* `rotation-y`: Rotate the circle in an angle on Y axis
  * default is `0`
* `rotation-z`: Rotate the circle in an angle on Z axis
  * default is `0`

Example:

<pre class="language-json"><code class="lang-json">"PARTICLE_CIRCLE": {
  "rotation-x": 90,
  "target": "LOCATION",
<strong>  "viewers": "ALL",
</strong><strong>  "radius": 1.25,
</strong>  "fill": true,
  "density": 0.6,
  "particle-data": {
    "particle": "LARGE_SMOKE"
  }
}
</code></pre>
