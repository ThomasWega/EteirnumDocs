---
description: Amount of current mana
---

# MANA

### Mana Food Level Calculation

Calculates the level (progress) of the food bar based on the current MANA. This formula is used:

$$
\text{{manaFoodLevel}} = 20 \times \left(\frac{{\text{{mana}}}}{{\text{{totalMaxMana}}}}\right)
$$

#### Where:

* `manaFoodLevel` — the calculated mana food level
* `mana` — the current mana
* `totalMaxMana` — base max mana + any other
