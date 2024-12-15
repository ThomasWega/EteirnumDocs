---
description: Trace a straight line and potentially check for certain collisions
---

# RAYTRACE

## Parameters:

* `max-distance`: Max distance to trace
* `ray-size`: Size of the ray line
  * default is `0.75`
* `ray-step`: Step length to take on each next check
  * default is `0.2`
* `transparent`: Whether to only allow the ray line to pass through transparent materials
  * default is `false`
* `pass-through`: Whether to only allow the ray line to pass through pass-through materials
  * default is `false`
* `entities`: Whether to check for entity collisions or skip them completely
  * default is `true` (check for collisions)
  * can improve performance if only step-effects like particles are used
* `entity-limit`: Limit the amounts of entities the ray line will go through before stopping
  * default is `1`
* `start-offset`: Offset where the ray line starts from
  * default is `0`
* `hit-effects`: Effects to run for each entity the ray line hit
  * default is `none`
* `step-effects`: Effects to run on each next step of the ray line
  * default is `none`
* `end-effects`: Effects to run at the last location of the ray line
  * will run even if no collision was made

Example:

```json
{
  "RAYTRACE": {
    "target": "INVOKER",
    "max-distance": 15,
    "transparent": false,
    "pass-through": false,
    "ray-size": 1,
    "effects": [
      {
        "MSG": {
          "type": "CHAT",
          "target": "TARGET",
          "msg": "<#FF7C17>{invoker} unleashed a burst of fire!"
        }
      }
    ]
  }
}
```
