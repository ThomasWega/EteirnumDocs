---
description: Group multiple effects together and apply them
---

# EFFECTS

## Parameters:

* `effects`: Effects to execute on every iteration

Example:

```json
"effects": [
  {
    "APPLY_SKILL": {
      "ignore-unapply": true,
      "propagate": true,
      "skill-id": "circle"
    }
  },
  {
    "EFFECTS": {
      "conditions": [
        "%skill_circle%==false"
      ],
      "effects": [
        {
          "POTION": {
            "propagate": true,
            "target": "TARGET",
            "potion": "blindness",
            "extend": true,
            "duration-ticks": 200,
            "amplifier": 1
          }
        },
        {
          "PARTICLE_CIRCLE": {
            "rotation-x": 90,
            "target": "LOCATION",
            "viewers": "ALL",
            "particle": "LARGE_SMOKE",
            "radius": 1.25,
            "fill": true,
            "density": 0.6
          }
        },
        {
          "SOUND": {
            "conditions": [
              "%first_apply%==true"
            ],
            "propagate": true,
            "target": "TARGET",
            "viewers": "ALL",
            "sound": "entity.wither.hurt",
            "volume": 0.12,
            "pitch": 1.2
          }
        }
      ]
    }
  }
]
```

In this example, we can see that the part after `EFFECTS` and all effects inside of it are only applied when skill circle is not used
