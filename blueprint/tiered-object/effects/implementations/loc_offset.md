---
description: Offsets the currently set location
---

# LOC\_OFFSET

## **Parameters**:

* All [Parameters of `LOC_SET` effect](loc_set.md)
* `min-spread-x`: The minimal distance offset to X direction
  * default is `none`
* `min-spread-y`: The minimal distance offset to Y direction
  * default is `none`
* `min-spread-z`: The minimal distance offset to Z direction
  * default is `none`
* `max-spread-x`: The maximal distance offset to X direction
  * default is `none`
* `max-spread-y`: The maximal distance offset to Y direction
  * default is `none`
* `max-spread-z`: The maximal distance offset to Z direction
  * default is `none`

{% hint style="warning" %}
If spreads are used, both min and max spread needs to be set for the direction
{% endhint %}

Example:

```json
"LOC_OFFSET": {
  "ignore-unapply": true,
  "x": [-1, 1],
  "y": [-0.2, 0.2],
  "z": [-1, 1]
}
```

```json
"LOC_OFFSET": {
  "target": "LOCATION",
  "ignore-unapply": true,
  "propagate": true,
  "min-spread-x": 0.4,
  "max-spread-x": 1.0,
  "min-spread-z": 0.4,
  "max-spread-z": 1.0
}
```
