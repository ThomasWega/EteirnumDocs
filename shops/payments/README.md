---
description: Specify the buy/sell logic and required stuff to make a transaction
---

# Payments

Contains two types. Buy and sell. They are optional, meaning if you don't want to allow selling of the product, you don't include the sell section.

{% hint style="warning" %}
Different types of payments may require different parameters.
{% endhint %}

## Parameters

These parameters apply to every Payment Type.

* `type`: type implementation of the payment
* `amount`: amount to be sold on one purchase

Example:

```json
"requirement": {
  "buy": {
    "type": "MATERIAL",
    "material": "BEDROCK",
    "amount": 1
  },
  "sell": {
    "type": "MATERIAL",
    "material": "BARRIER",
    "amount": 1
  }
}
```

