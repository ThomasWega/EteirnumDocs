---
description: Set's a place where the player should spawn after being killed
---

# SPAWN\_POINT

## Parameters:

* All [Parameters of `LOC_SET` effect](loc_set.md)
* `uses`: How many times the spawn point can be used for before being erased
  * default is `1`
* `respawn-effects`: Effects to run when the user uses the spawnpoint
  * default is `none¨`

{% hint style="warning" %}
Don't forget to set [`stop-on-death`](../shared-parameters/stop-on-death.md) to `false`.
{% endhint %}

Example:

```json
"SPAWN_POINT": {
  "stop-on-death": false,
  "ticks": [0, 400],
  "respawn-effects": [
    {
      "MSG": {
        "type": "ACTION_BAR",
        "msg": "<color:#ff8a8a>Respawned at your temporary spawn point!</color>"
      }
    },
    {
      "SOUND": {
        "ignore-unapply": true,
        "viewers": "INVOKER",
        "sound": "block.respawn_anchor.deplete",
        "volume": 1,
        "pitch": 0.7
      }
    },
    {
      "UNAPPLY_EFFECTS": {}
    }
  ]
}
```
