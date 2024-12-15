---
description: Conditions that need to be passed in order to apply the effect
---

# Conditions

Any [Placeholder](https://app.gitbook.com/o/y2atbaFomvwTmsuxAKt7/s/8UBjQvIReVfhUCzFe6Gs/) can be used. If `true` or `1` is returned, the condition passes. Otherwise if even one condition fails to pass, the effect won't be executed

{% hint style="info" %}
If result is a number, trailing decimal zeroes will be removed for the check. So `1.000` will become `1` and the condition will still pass
{% endhint %}

Example:

```json
"MSG": [
  {
    "conditions": [
      "%math_{player_health} > ({player_max_health} / 2)%"
    ],
    "type": "CHAT",
    "msg": "<green>Your health is above half!"
  },
  {
    "conditions": [
      "%math_{player_health} < ({player_max_health} / 2)%"
    ],
    "type": "CHAT",
    "msg": "<red>Your health is below half!"
  }
]
```
