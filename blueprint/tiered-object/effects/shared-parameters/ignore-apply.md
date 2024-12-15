---
description: Don't activate the effect the first iteration
---

# Ignore Apply

TODO: add valid usage example

Usage of this is pretty scarce, however it might be useful in some edge cases. If you use this approach a lot, you might be using incorrect approach though. Check the warning below to understand why

{% hint style="info" %}
By default `ignore-apply` is `false`
{% endhint %}

Example:

```json
"IN_RANGE": {
  "ignore-apply": true,
  "radius": 3,
  "ticks": [0, 12, 4, 4, 20, 4, 4, 20, 4, 4],
  "repeat": 9,
  "effects": []
}
```

First apply is instant ([0 ticks](ticks.md)), but is ignored, so the first is a [repeat](repeat.md) , which is delayed by [12 ticks](ticks.md).

{% hint style="danger" %}
In this example the `ignore-apply` is useless, as a better approach specified below provides clearer initiative
{% endhint %}

```json
"IN_RANGE": {
  "radius": 3,
  "ticks": [12, 4, 4, 20, 4, 4, 20, 4, 4],
  "repeat": 8,
  "effects": []
}
```

First apply will be [12 ticks](ticks.md) delay, then [4 ticks](ticks.md) repeats

{% hint style="success" %}
This would be the correct approach
{% endhint %}
