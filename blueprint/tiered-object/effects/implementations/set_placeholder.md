---
description: Sets placeholder which can later on by used on a different effect
---

# SET\_PLACEHOLDER

## Parameters:

* `key`: Any text to use as the placeholder
* `value`: Value of the placeholder
* `overwrite`: Whether to overwrite the current placeholder value (if any)
  * default is `true`

Example:

```json
"effects": [
  {
    "SET_PLACEHOLDER": {
      "propagate": true,
      "key": "%particle%",
      "value": "GLOW"
    }
  },
  {
    "PARTICLE_CIRCLE": {
      "propagate": true,
      "ticks": 20,
      "repeat": 10
      "rotation": 90,
      "particle": "%particle%",
      "radius": 1,
      "count": 8,
      "y": 1
    }
  },
  {
    "LISTENER": {
      "propagate": true,
      "ticks": [0, 200],
      "event": "ATTACK_PLAYER",
      "effects": [
        {
          "SET_PLACEHOLDER": {
            "propagate": true,
            "key": "%particle%",
            "value": "FLAME"
          }
        }
      ]
    }
  }
]
```

In this example, the particle will first be `GLOW`, but if player is hit, it will become `FLAME`
