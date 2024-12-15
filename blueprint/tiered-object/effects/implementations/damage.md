---
description: Damage an entity
---

# DAMAGE

## **Parameters**:

* `damage`: Amount of damage. More info [here](damage.md#damage)
* `cause`: The cause of the damage. List [here](damage.md#cause)
* `force-critical`: Always recognize the damage as critical
  * default is `false`

### Damage

If no damage is specified, the damage will be calculated based on players attributes as on usual attack (ATTACK, DEFENSE etc.)

### Cause

* `MELEE`
* `SPELL`

Example:

```json
"DAMAGE": {
  "damage": 1,
  "cause": "SPELL",
  "force-critical": false
}
```
