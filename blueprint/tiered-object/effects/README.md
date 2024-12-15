---
description: Determines what happens when item is used/activated
---

# Effects

Effects are optional. If the JSON array is empty or the "effects" are not in the JSON at all, no effects will be applied.

## Components

1. **Type**: Specifies the type of effect. List [here](implementations/)
2. **Parameters**: Parameters required for each effect type. Every type implementation has these [default shared parameters](shared-parameters/). You can see the specific parameters for each type in their corresponding [type implementations documentation](../implementations/)

### Random/Multiple values in [Parameters](./#components)

Ranges specify the range/array of numbers. (depends on the implementation)

There are multiple ways to format a range. The most often used is:

```json
range: [2, 4]
```

However, if the range has same min and max you can also use:

```json
range: 2
```

This is also a valid format

```json
range: [2]
```

{% hint style="warning" %}
Even though your JSON editor will probably format the range numbers on new lines, please keep one of these formats. They are much more readable in the final blueprint.
{% endhint %}

```json
// Don't use this format
range: [
    2, 
    4
]
```

In some places, arrays can also be used to set up order of multiple things. These go in order and are not random! Here's an example

```json
array: [2, 4, 6, 8, 10]
```

## Using Math in effects

Almost every parameter for every effect not only parses placeholders, but can also do pretty complex math. EvalEx is used under the hood and it even works when including placeholders (even the custom ones)

Here are some examples:

```
!(true)
%loc_x%==100.2
ROUND(%loc_y%, 2)=10.22
```

{% embed url="https://ezylang.github.io/EvalEx/references/references.html" %}
For all possible usages take a look at these documentations:
{% endembed %}

{% hint style="warning" %}
EvalEx doesn't support text comparison! Use [String](https://api.extendedclip.com/expansions/string/) expansion for PlaceholderAPI
{% endhint %}

## Multiple same effects

{% hint style="warning" %}
If you use one effect multiple times in the same effects block, formatting it this way might not make the best sense
{% endhint %}

```json
"effects": [
  {
    "ATTRIBUTE_MODIFIER": {
    "ticks": 320,
    "attribute": "ATTACK_DAMAGE",
    "range": [1],
    "logic": "MULTIPLIER",
    "display": "NONE",
    "type": "STATIC"
    }
  },
  {
    "ATTRIBUTE_MODIFIER": {
    "ticks": 320,
    "attribute": "SPEED",
    "range": [1],
    "logic": "MULTIPLIER",
    "display": "NONE",
    "type": "STATIC"
    }
  }
]
```

While it might work fine, this formatting is much more clean

{% hint style="success" %}
This way it's obvious there are multiple ATTRIBUTE\_MODIFIER effects, so they are all put together in the same block
{% endhint %}

```json
"effects": [
  {
    "ATTRIBUTE_MODIFIER": [
      {
        "ticks": [0, 320],
        "attribute": "ATTACK_DAMAGE",
        "range": 1,
        "logic": "MULTIPLIER",
        "display": "NONE",
        "type": "STATIC"
      },
      {
        "ticks": [0, 320],
        "attribute": "SPELL_DAMAGE",
        "range": 1,
        "logic": "MULTIPLIER",
        "display": "NONE",
        "type": "STATIC"
      }
    ]
  }
]
```

## Placeholders

Almost all effects allow the usage of placeholders in [Parameters](./#components).

Any PlaceholderAPI placeholder including [ours placeholders ](https://app.gitbook.com/o/y2atbaFomvwTmsuxAKt7/s/8UBjQvIReVfhUCzFe6Gs/)can be used.

Just replace the number with placeholder surrounded with `"`. Here is an example:

```json
"DAMAGE": {
  "damage": "%player_health%",
  "cause": "SPELL",
}
```

## Viewable Effects

Sometimes you have effects which you might want to apply for one target only, but allow multiple targets seeing it. This is where Viewable Effects come into play. These effects allow you to specify [Targets](./#targets) which should see the effect as well. Most notable example could be the [PARTICLE](implementations/particle.md) effect.

Viewer can always only be a player.

If viewers parameter is supported on the effect. It will be stated inside the effect's page description

Here is an example:

```json
"PARTICLE": {
  "target": "LOCATION",
  "viewers": ["INVOKER", "TARGET"],
  "particle": "SWEEP_ATTACK",
}
```

### Targets

* INVOKER
* TARGET
* ALL
  * every player (if not limited by the server)
