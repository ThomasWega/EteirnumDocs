---
description: Change the currently set location
---

# LOC\_SET

## **Parameters**:

* `x`: New X  location
  * if none set, won't be changed
* `y`: New Y location
  * if none set, won't be changed
* `z`: New Z location
  * if none set, won't be changed
* `yaw`: New yaw location
  * if none set, won't be changed
* `pitch`: New pitch location
  * if none set, won't be changed
* `world`: New world
  * if none set, won't be changed

Example:

```json
"LOC_SET": {
  "target": "LOCATION",
  "ignore-unapply": true,
  "propagate": true,
  "x": "%loc_x%_+10",
}
```
