---
description: Reduction of damage
---

# DEFENSE

### Damage Reduction Calculation

$$
\text{finalDamage} = \text{totalDamage} \times \left( \frac{100}{100 + \text{totalDefense}} \right)
$$

#### Where:

* `finalDefense` — calculated defense to deduct on finalDamage
* `totalDamage` — base damage + any other
* `totalDefense` — base defense + any other
