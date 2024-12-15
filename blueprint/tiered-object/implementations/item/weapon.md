---
description: Holdable weapon
---

# Weapon

## Game class

It is required to provide what game class this weapon belongs to. The reason for this is to allow per-class use of [Spell](../spell.md) when holding these weapons.&#x20;

If the player's game class equals the weapon's game class, the [Spells](../spell.md) with same game class will be allowed to be cast. If this is not the case, only spells from the default game class will be allowed to be cast

Example:

```json
{
  "id": "sword",
  "impl": "WEAPON",
  "game-class": "REVENANT",
  "tiers": []
}
```
