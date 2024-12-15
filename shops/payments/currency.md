---
description: Requires a specific amount of physical currency in the shoppers inventory
---

# CURRENCY

## Parameters

* `currency`: type of the physical currency
* `tier`: tier of the physical currency.&#x20;
  * tier conversions will be made automatically on transaction

Example:

```json
"buy": {
  "type": "PHYSICAL_CURRENCY",
  "currency": "GOLD_RAW",
  "tier": "TIER_1",
  "amount": 10
}
```

