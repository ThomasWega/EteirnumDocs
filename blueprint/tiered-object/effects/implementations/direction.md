---
description: Modify the direction
---

# DIRECTION

## Parameters:

* `forward`: Multiplier applied to the forward direction
  * default is `1.0`
* `upward`: Multiplier applied to the forward direction
  * default is `1.0`
* `right`: Multiplier applied to the right direction
  * default is `1.0`
* `yaw`: Yaw to apply to direction
* `pitch`: Pitch to apply to direction
* `add-to-velocity`: Whether the calculated directional velocity should be added to the current velocity
  * default is `false`
* `set-on-target`: Whether to set the new velocity to the target entity
  * default is `false`

Example:

```json
"DIRECTION": {
  "forward": 5,
  "add-to-velocity": false
}
```
