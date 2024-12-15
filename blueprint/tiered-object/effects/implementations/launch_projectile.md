---
description: Launch a projectile in location direction
---

# LAUNCH\_PROJECTILE

## Parameters:

* `projectile`: Type of the projectile. List [here](launch_projectile.md#projectile)
* `velocity`: Velocity multiplier (speed + how far the projectile will go)
  * default is `1.0`

### Projectile

* `ARROW`
* `FIREBALL`

{% hint style="warning" %}
When projectile is fired, it's set as the new [`TARGET`](../shared-parameters/target.md)
{% endhint %}

Example:

```json
"LAUNCH_PROJECTILE": {
  "ticks": [0, 60],
  "projectile": "FIREBALL",
  "velocity": 2,
}
```
