---
description: Weapons/Tools/Armor
---

# Item

Gear activates on item equip/hold

## Item

There are additional placeholder provided for item generation.

* `<quality>` - Shows the [Quality](./#qualities) display name
* `<modifiers>` - Shows list of [Modifiers](./#modifiers) display names. Each modifier on a new line

Example:

```json
"item": {
  "material": "WOODEN_SWORD",
  "display": "<#8B5A2B>Wooden Sword",
  "lore": [
    "<yellow>Tier 1",
    "<quality>",
    "",
    "<modifiers>"
  ]
}
```

## Qualities

Each gear blueprint can have it's own qualities inside the tier configuration.

Example:

```json
"qualities": [
  {
    "id": "common",
    "display": "COMMON",
    "color": "<#FFFFFF>",
    "drop-chance": 0.5,
    "modifiers": 1
  },
  {
    "id": "unique",
    "display": "UNIQUE",
    "color": "<#8AFF91>",
    "drop-chance": 0.35,
    "modifiers": 2
  },
  {
    "id": "rare",
    "display": "RARE",
    "color": "<#A5F1FF>",
    "drop-chance": 0.09,
    "modifiers": 3
  },
  {
    "id": "legendary",
    "display": "LEGENDARY",
    "color": "<#F6FF00>",
    "drop-chance": 0.05,
    "modifiers": 4
  },
  {
    "id": "godly",
    "display": "GODLY",
    "color": "<#C800E3>",
    "drop-chance": 0.01,
    "modifiers": 5
  }
]
```

## Required Modifiers

This field is completely optional, but allows you to force modifiers onto the gear. Every gear generated from that blueprint will have that modifier preset. Modifier values will be taken from the [Modifiers](./#modifiers) section, so make sure the required modifier is setup there as well.

Example:

```json
"required-modifiers": [
  "MAX_HP",
  "DEFENSE"
]
```

## Modifiers

This field allows you to configure the modifiers that might be applied to the gear. On gear generation, the quality is first generated and from that the amount of modifiers is determined. Then the target amount of modifiers are randomly selected from this section and their values are applied accordingly.

Example:

```json
"modifiers": [
  {
    "attribute": "MAX_MANA",
    "range": [60, 100],
    "logic": "FLAT",
    "display": "NONE",
    "type": "STATIC"
  },
  {
    "attribute": "HP_REGEN_AMOUNT",
    "range": [0.08, 0.12],
    "logic": "PERCENTAGE",
    "display": "NONE",
    "type": "STATIC"
  },
  {
    "attribute": "MANA_REGEN_AMOUNT",
    "range": [0.12, 0.18],
    "logic": "PERCENTAGE",
    "display": "NONE",
    "type": "RANDOM"
  },
  {
    "attribute": "HP_REGEN_TICKS",
    "range": [-12, -8],
    "logic": "FLAT",
    "display": "SECONDS",
    "type": "STATIC"
  },
  {
    "attribute": "CRIT_MULTIPLIER",
    "range": [0.05, 0.2],
    "logic": "MULTIPLIER",
    "display": "NONE",
    "type": "STATIC"
  },
]
```

These are basically just [ATTRIBUTE\_MODIFIER](../../effects/implementations/attribute_modifier.md) effect that activate on gear equip/hold
