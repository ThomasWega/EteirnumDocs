---
description: Increases chance of finding good loot
---

# RARITY\_FINDER

### Drop Chance Calculation

Items are ordered based on their drop chance. The lowest chance (rarest) first. Then this formula is used

$$
\text{finalDropChance} = \text{{dropChance}} \times \text{{totalRarityFinder}}
$$

#### Where:

* `finalDropChance` — calculated chance that is then randomly tried to pass
* `dropChance` — drop chance of the item
* `totalRarityFinder` — base rarity finder + any other

This is then used to try to pass the chance of the item with the lowest chance. Basically this calculation just increases the chance of every item, starting from the lowest chanced (rarest) ones
