---
description: Exp used to calculate level and progress till next level
---

# EXP

### Level Calculation Formula

&#x20;The level is calculated from the experience points (XP) using the following formula:

$$
\text{level} = \left\lfloor \sqrt{\frac{\text{exp}}{1000}} \right\rfloor
$$

#### Where:

* `level` — the current level&#x20;
* `exp` — the current experience points

### Experience Required for a Level&#x20;

The experience required for a level is calculated using the following formula:

$$
\text{exp} = \text{level}^2 \times 1000
$$

#### Where:

* `exp` — the experience required for the current level&#x20;
* `level` — the current level

### Experience Required for the Next Level

The experience required for the next level is calculated using the following formula:

$$
\text{nextLevelExp} = (\text{level} + 1)^2 \times 1000
$$



#### Where:

* `nextLevelExp` — the experience required for the next level&#x20;
* `level` — the current level

### Experience Missing for the Next Level

The experience missing for the next level is calculated using the following formula:

$$
\text{missingExp} = \text{nextLevelExp} - \text{currentExp}
$$

#### Where:

* `missingExp` — the experience missing for the next level&#x20;
* `nextLevelExp` — the experience required for the next level&#x20;
* `currentExp` — the current experience points

### Progress Towards the Next Level

The progress towards the next level is calculated using the following formula:

$$
\text{progress} = \frac{\text{currentExp} - \text{levelExp}}{\text{nextLevelExp} - \text{levelExp}}
$$

#### Where:

* `progress` — the progress towards the next level as a float between 0 (just reached the current level) and 1 (just about to reach the next level)&#x20;
* `currentExp` — the current experience points&#x20;
* `levelExp` — the experience required for the current level&#x20;
* `nextLevelExp` — the experience required for the next level
