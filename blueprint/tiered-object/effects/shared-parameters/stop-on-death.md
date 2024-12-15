---
description: Whether the effect should be stopped on target's death
---

# Stop On Death

If the effect is scheduled (using [Ticks](ticks.md) or [Repeats](repeat.md)), the target might die before the effect was applied or while it's being applied. For potions and other things, you might want to cancel the activation of the effects in that case.

{% hint style="info" %}
By default `stop-on-death` is `true`
{% endhint %}

Example:

```json
"ATTRIBUTE_MODIFIER": {
  "stop-on-death": true,
  "ignore-unapply": true,
  "ticks": 60,
  "repeat": 2,
  "attribute": "HP",
  "range": 10,
  "type": "STATIC"
}
```
