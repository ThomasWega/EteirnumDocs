---
description: Defining Tiers
---

# Tiers

Each tier within a blueprint can have its own set of properties, including item details, effects, and attributes.

## Item Parameters

* `material`: The material type of the item.
  * should be in `UPPER_CASE`
* `display`: The display name of the item, which can include color codes.
* `lore`: A description or lore of the item.
* `custom-model`: Custom model data number of the item
  * exclude to not set any model

Example:

```json
"item": {
  "material": "POTION",
  "display": "<blue>HP Potion",
  "lore": [
    "<yellow>Tier 1"
  ]
  "custom-model": 132
}
```

Some implementations might have placeholders, that can be used in display/lore

## [Effects](effects/)

Effects define what happens when the item is used or activated. They can modify attributes, display messages, create particles, play sounds, etc.

