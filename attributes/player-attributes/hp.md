---
description: Health points
---

# HP

### Health Level Calculation

Stands for the Minecraft health bar value. The health level of the player is calculated using the following formula:

$$
\text{healthLevel} = \left( \frac{\text{hp}}{\text{maxHp}} \right) \times \text{maxHealthLevel}
$$

#### Where:

* `healthLevel` — the health level of the player hp is the current health points of the player&#x20;
* `maxHp` — the maximum health points of the player
* `maxHealthLevel` — the maximum health level of the player

### Max Health Level Calculation

$$
\text{maxHealthLevel} = \left( \frac{\text{maxHp}}{\text{HP\_CAP}} \right) \times \text{BUKKIT\_HP\_CAP}
$$

#### Where:

* `maxHealthLevel` — the maximum health level of the player&#x20;
* `maxHp` — the maximum health points of the player
* `HP_CAP` — the HP cap
  * Currently `100`
* `BUKKIT_HP_CAP` — the maximum Minecraft health allowed
  * Currently `20` (full health bar)

### Extra Health Level Calculation

The extra health level of the player is calculated using the following formula:

$$
\text{extraHealthLevel} = \max \left( 0, \left( \frac{\text{hp} - \text{baseMaxHp}}{\text{EXTRA\_HP\_CAP}} \right) \times \text{BUKKIT\_EXTRA\_HP\_CAP} \right)
$$

#### Where:

* `extraHealthLevel` — the extra health level of the player&#x20;
* `hp` — the current health points of the player&#x20;
* `baseMaxHp` — the base maximum health points of the player
* `EXTRA_HP_CAP` — the extra HP cap
  * Currently `100`
* `BUKKIT_EXTRA_HP_CAP` - the maximum Minecraft absorption health allowed
  * Currently `20` (one full bar)
