---
description: HP stolem on attack from the damaged entity and given to the attacker
---

# LIFE\_STEAL

### Total HP Add Calculation

Calculates how many HP are added to the attacker. Uses this formula:

$$
\text{finalLifeSteal} = \text{{totalDamage}} \times \text{{totalLifeSteal}} \times \text{{LIFE\_STEAL\_PERCENTAGE}}
$$

#### Where:

* `finalLifeSteal` — calculated HPs to give to the attacker
* `totalDamage` — base damage + any other
* `totalLifeSteal` — base life steal + any other
* `LIFE_STEAL_PERCENTAGE` — Percentage of HP  to take
  * currently `5%` (0.05)
