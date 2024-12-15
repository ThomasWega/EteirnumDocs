---
description: Castable spells
---

# Spell

Spells activate effects on spell cast

## Skills

Skills are used to set certain parameters and values before applying the actual effects. This can be useful, when you want to have a purchasable upgrade for spell, which might for example increase the radius or damage.

Skills can be combined with each other.

Skills are saved and applied in order and are being recognized by their index inside of the `skills` array block.

### Parameters

* `id`: Unique identification for the skill
* `tier`: Same parameters as the [Tiers](../tiers.md)

Example usage:

```json
{
  "id": "assimilation_of_void",
  "game-class": "REVENANT",
  "impl": "SPELL",
  "skills" : [
    {
      "skill": {
        "id": "55%_heal",
        "tier": {
          "item": {
            "material": "SHIELD",
            "display": "<#4D4748>Assimilation of Void",
            "lore": [
              "● Heals 55% of max HP"
            ]
          },
          "effects": [
            {
              "SET_PLACEHOLDER": {
                "ignore-unapply": true,
                "propagate": true,
                "key": "%heal_percentage%",
                "value": "0.55"
              }
            }
          ]
        }
      }
    }
  ],
  "tiers": [
    {
      "item": {
        "material": "ENDER_EYE",
        "display": "<#4D4748>Assimilation of Void",
        "lore": [
          "● Heals 40% of max HP"
        ]
      },
      "effects": [
        {
          "SET_PLACEHOLDER": [
            {
              "ignore-unapply": true,
              "propagate": true,
              "key": "%heal_percentage%",
              "value": "0.4"
            }
          ]
        },
        {
          "APPLY_SKILL": {
            "ignore-unapply": true,
            "propagate": true,
            "skill-id": "55%_heal"
          }
        },
        {
          "ATTRIBUTE_MODIFIER": {
            "ignore-unapply": true,
            "attribute": "HP",
            "range": "%eteirnumcore_attributes_total_true_max_hp%*%heal_percentage%",
            "logic": "FLAT",
            "display": "NONE",
            "type": "RANDOM"
          }
        }
      ]
    }
  ]
}
```

In this example, we can see that if a skill is used, the placeholder `%heal_percentage%` is set to `0.55` (55%). The [`APPLY_SKILL`](../effects/implementations/apply_skill.md) effect here is only activated if the [Target](../effects/shared-parameters/target.md) has the skill applied

## Game class

It is required to provide what game class this spell belongs to. It's then used in combination with the [Weapon](item/weapon.md#game-class) currently being held. If the player's game class does not match the spells game class, the spell cannot be cast and won't be allowed to, neither will it be suggested in the action bar to the player.

Example:

```json
{
  "id": "blitz",
  "game-class": "REVENANT",
  "overwrite": true,
  "impl": "SPELL"
}
```

## Overwrite

Optional parameter, which allows to specify whether the current blueprint should be overwritten if is applied again before all effects being unapplied first.

Example:

```json
{
  "id": "hellfire_barrage",
  "game-class": "MAGUS",
  "overwrite": true,
  "impl": "SPELL",
  "skills": [],
  "tiers": []
}
```

{% hint style="info" %}
By default the `overwrite` is `false`
{% endhint %}
