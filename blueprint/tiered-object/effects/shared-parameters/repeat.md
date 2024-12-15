---
description: Number of repetitions (iterations) of the effect
---

# Repeat

{% hint style="info" %}
By default `repeat` is `0 (none)`
{% endhint %}

Example:

```json
"ATTRIBUTE_MODIFIER": {
  "ignore-unapply": true,
  "attribute": "HP",
  "repeat": 2
  "ticks": 20
  "range": 20,
  "type": "STATIC"
}
```

This will add 20 HP every [20 ticks](../../tiers.md). Will be repeated 3 times total

{% hint style="info" %}
First apply is not recognized as a repeat! Unless [`ignore-apply`](ignore-apply.md) is set, effect with 2 repeats will be run 3 times.
{% endhint %}

{% hint style="warning" %}
If any value was already set by any repeat (iteration), the value will be unapplied!
{% endhint %}

## Placeholders

Any valid number PlaceholderAPI placeholers including [ours placeholders](https://app.gitbook.com/o/y2atbaFomvwTmsuxAKt7/s/8UBjQvIReVfhUCzFe6Gs/), can be used to declare the repeat count. Here is an example:

```json
"ATTRIBUTE_MODIFIER": {
  "ignore-unapply": true,
  "repeat": "%player_no_damage_ticks%"
  "attribute": "HP",
  "range": 20,
  "logic": "FLAT",
  "type": "STATIC"
}
```
