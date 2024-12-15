---
description: Listen for event call
---

# LISTENER

## **Parameters**:

* `event`: Event to listen for. List [here](listener.md#event)
* `listen-limit`: Limit the number of times the event will be listened to
  * default is `1`
* `effects`: Effects to execute when the event is called

### Event

* `ATTACK_PLAYER` - Player attacks player
* `PROJECTILE_HIT` - When a projectile, like FIREBALL or ARROW hits

Example:

```json
"LISTENER": {
  "ticks": [0, 60],
  "event": "ATTACK_PLAYER",
  "effects": [
    {
      "MSG": {
        "type": "CHAT",
        "msg": "<yellow>You have attacked with Decimation!"
      }
    }
  ]
}
```

This example will listen for `ATTACK_PLAYER` event for [60 ticks](../shared-parameters/ticks.md). If before this duration a player attacks other player, a message will be sent to the attacker
