---
description: Don't activate the effect the last iteration (repeat)
---

# Ignore Unapply

{% hint style="info" %}
By default `ignore-unapply` is `false`
{% endhint %}

Example:

```json
"ATTRIBUTE_MODIFIER": {
  "ignore-unapply": true,
  "attribute": "HP",
  "range": 10,
  "type": "STATIC"
}
```

In this example, we don't want to unapply the HP after applying it. We want the player to keep it.
