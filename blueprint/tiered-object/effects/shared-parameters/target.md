---
description: Target to apply the effect for
---

# Target

* `INVOKER`
  * applies to the invoker
* `TARGET`
  * applies to the target (e.g on attack the damaged player)
  * depends on implementation
* `LOCATION`
  * applies to the location of effect activation (e.g. on attack where the damaged player stood)
  * depends on implementation

{% hint style="info" %}
By default `target` is `INVOKER`
{% endhint %}

Example:

```json
"LISTENER": {
  "ticks": [0, 60],
  "event": "ATTACK_PLAYER",
  "effects": [
    {
      "IN_RANGE": {
        "radius": 3,
        "ticks": 20,
        "repeat": 2,
        "effects": [
          {
            "PARTICLE": {
              "target": "LOCATION",
              "particle": "SWEEP_ATTACK",
              "count": 1
            }
          }
        ]
      }
    }
  ]
}
```

Here we can see that inside the `PARTICLE` effect, we set the target to `LOCATION`. We are listening for `ATTACK_PLAYER` for [60 ticks](ticks.md), which will set the location to the damaged target current location and save it. What this will produce is that after the player was attacked, on the location of the attack after first [20 ticks](ticks.md) delay, it will keep spawning `SWEEP_ATTACK` particles [3 times](repeat.md) with [20 ticks](ticks.md) interval in between. If we did not set the target to `LOCATION`, it would default to last set target (which by default is `INVOKER`) and gets it's location

```json
"LISTENER": {
  "ticks": [0, 60],
  "event": "ATTACK_PLAYER",
  "effects": [
    {
      "MSG": {
        "target": "TARGET",
        "type": "CHAT",
        "msg": "<yellow>You have attacked with Decimation!"
      }
    }
  ]
}
```

In this example the message will be sent to `TARGET` (the damaged player). If we did not change the target, it would be set to `INVOKER` instead.&#x20;

## Multiple Targets

You can also use multiple targets at once. Here is an example of how to do that

```json
"MSG": {
  "target": ["INVOKER", "TARGET"],
  "type": "CHAT",
  "msg": "<yellow>You have attacked with Decimation!"
}
```
