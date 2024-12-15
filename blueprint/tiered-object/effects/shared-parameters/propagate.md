---
description: Toggle whether to propagate the modified parameters with other effects
---

# Propagate

In certain effects, you might want to use different targets, or modify the locations. This toggle will specify whether that change should be passed to other effects as well, or apply only on the current effect.

{% hint style="info" %}
By default `propagate` is `false`
{% endhint %}

Example:

```json
"effects": [
  {
    "LOC_OFFSET": {
      "propagate": true,
      "ignore-unapply": true,
      "x": [-1, 1],
      "y": [-0.2, 0.2],
      "z": [-1, 1]
     }
  },
  {
    "PARTICLE": {
      "target": "LOCATION",
      "particle": "SWEEP_ATTACK",
      "count": 1,
      "x": 0,
      "y": 1.25,
      "z": 0
    }
  }
]
```

In this example. we want to share the parameters, to make the `PARTICLE` spawn on the modified location
