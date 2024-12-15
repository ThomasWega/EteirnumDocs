---
description: Damage when attacking an entity
---

# ATTACK\_DAMAGE

### Total Attack Damage Calculation

If damage is deemed as citical (by passing a chance), this formula is used:

$$
\text{finalDamage} = \text{{totalDamage}} \times \text{{totalCritMultiplier}}
$$

#### Where:

* `finalDamage` — calculated damage to be applied
* `totalDamage` — base damage before calculating modifiers (life steal, defense etc.) + any other
* `totalCritMultiplier` — base crit multiplier + any other
