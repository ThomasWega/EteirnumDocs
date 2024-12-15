---
description: Unlocks a Skill on a Spell
---

# SPELL\_SKILL

## Parameters

* `spell-id`: ID of the spell, as defined in it's [Blueprint](https://app.gitbook.com/s/PEypf6i3dQewsaETmwpg/tiered-object/implementations/spell)
* `skill-id`: ID of the skill on the spell, as defined in it's [Blueprint](https://app.gitbook.com/s/PEypf6i3dQewsaETmwpg/tiered-object/implementations/spell#skills)

Example:

```json
"skills": [
  {
    "bind-id": "dusk_ward_5_attacks_skill",
    "type": "SPELL_SKILL",
    "spell-id": "dusk_ward",
    "skill-id": "5_attacks"
  }
]
```
