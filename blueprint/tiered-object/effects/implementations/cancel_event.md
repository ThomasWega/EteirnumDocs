---
description: Cancels the event
---

# CANCEL\_EVENT

Needs to be used in combination with other effects

## Parameters:

* no parameters

Example:

```json
"LISTENER": {
  "ticks": [0, 100],
  "event": "ATTACK_PLAYER",
  "effects": [
    {
      "CANCEL_EVENT": {}
    }
  ]
}
```
