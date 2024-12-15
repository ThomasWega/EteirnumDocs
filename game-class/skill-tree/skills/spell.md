---
description: Rewards a new spell or new tier of spell
---

# SPELL

## Parameters

* `spell-id`: ID of the spell, as defined in it's [Blueprint](https://app.gitbook.com/o/y2atbaFomvwTmsuxAKt7/s/PEypf6i3dQewsaETmwpg/)
* `tier`: The tier of the spell
  * if player already has a higher tier, this skill will be ignored
  * if player already has a lower tier, his spell will be upgrades

Example:

```json
"skills": [
  {
    "bind-id": "dusk_ward",
    "type": "SPELL",
    "spell-id": "dusk_ward",
    "tier": 0
  }
]
```
