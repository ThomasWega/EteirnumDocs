---
description: >-
  Interval between activations of first/each iterations (repeats) or before
  unapply of effect
---

# Ticks

{% hint style="info" %}
By default `ticks` is `0 (instant)`
{% endhint %}

Example:

<pre class="language-json"><code class="lang-json">"ATTRIBUTE_MODIFIER": {
  "ticks": [0, 60],
<strong>  "attribute": "SPEED",
</strong>  "range": 0.2,
  "logic": "FLAT",
<strong>  "type": "STATIC"
</strong>}
</code></pre>

This will apply the effect after 0 ticks and remove after 60 ticks

{% hint style="success" %}
20 ticks = 1 second
{% endhint %}

Ticks can also be put into a [Range](../#range) and combined with [Repeats](ticks.md#repeat) to have different intervals between repeats

Example:

```json
"PARTICLE": {
  "ticks": [20, 3, 3, 3]
  "particle": "SWEEP_ATTACK",
  "count": 1,
  "repeat": 3
}
```

This will show `SWEEP_ATTACK` particle first time after 20 ticks, then [3 repeats](repeat.md) with 3 ticks delays each.

{% hint style="info" %}
If there is less number in `ticks` array than there are `repeat` iterations, the last number will always be used
{% endhint %}

## Placeholders

Any valid number PlaceholderAPI placeholers including [ours placeholders](https://app.gitbook.com/o/y2atbaFomvwTmsuxAKt7/s/8UBjQvIReVfhUCzFe6Gs/), can be used to declare the ticks amount. Here is an example:

```json
"ATTRIBUTE_MODIFIER": {
  "ignore-unapply": true,
  "ticks": "%player_health%"
  "attribute": "HP",
  "range": 20,
  "logic": "FLAT",
  "display": "NONE",
  "type": "STATIC"
}
```
