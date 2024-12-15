---
description: Products are the things that are being sold
---

# Products

The items (products) being sold in the selected [Category](categories.md) are specified here. Their buy/sell logic is also specified here. There are different types of products and they all have different parameters

## Parameters

* `name`: Name of the product
  * used in various messages
* `slot`: Slot in the products GUI of the category
* `display-item`: Item to be display on the `slot`. Same formatting as [here](https://app.gitbook.com/s/PEypf6i3dQewsaETmwpg/tiered-object/tiers#item-parameters)
* `requirement`: Requirement for purchase/sell. More info [here](payments/)
* `reward`: Reward received from buying/selling the item. Same logic as [`requirement`](payments/)

Example:

```json
"products": [
  {
    "name": "Example Item",
    "slot": 13,
    "display-item": {
      "material": "DIRT"
    },
    "requirement": {},
    "reward": {}
  }
]
```

