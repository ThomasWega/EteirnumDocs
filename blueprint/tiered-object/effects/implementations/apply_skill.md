---
description: Applies specified skill
---

# APPLY\_SKILL

More info [here](../../implementations/spell.md#skills)

## Parameters:

* `skill-id`: The unique id of a skill
* `force-apply`: Apply the skill even if the [Target](../shared-parameters/target.md) doesn't have it applied
  * Default is `false`, applying the skill only if the [Target](../shared-parameters/target.md) has it applied

Example:

```json
"APPLY_SKILL": {
  "ignore-unapply": true,
  "propagate": true,
  "skill-id": "5_attacks"
}
```
