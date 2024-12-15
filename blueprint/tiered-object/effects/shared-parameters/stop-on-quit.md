---
description: Whether the effect should be stopped when target quits
---

# Stop On Quit

If the effect is scheduled (using [Ticks](ticks.md) or [Repeats](repeat.md)), the target might quit before the effect was applied or while it's being applied. For potions and other things, you might want to cancel the activation of the effects in that case.

{% hint style="info" %}
By default `stop-on-quit` is `true`
{% endhint %}

Example:

```json
"ATTRIBUTE_MODIFIER": {
  "stop-on-quit": true,
  "ignore-unapply": true,
  "ticks": 60,
  "repeat": 2,
  "attribute": "HP",
  "range": 10,
  "type": "STATIC"
}
```
