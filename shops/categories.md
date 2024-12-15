---
description: Categorize the shop into different sections
---

# Categories

Categories allow you to separate the shop into different sections. This can be useful if you want to do a larger shop with items of different origin

{% hint style="warning" %}
If only one category is defined, the product GUI will be used right away
{% endhint %}

## Parameters

* `title`: Title of the category
* `rows`: Number of rows the product GUI of the category will have
* `slot`: Slot of this category inside of the categories GUI
* `display-item`: Item to be display on the `slot`. Same formatting as [here](https://app.gitbook.com/s/PEypf6i3dQewsaETmwpg/tiered-object/tiers#item-parameters)
* `fillers`: Slots of the fillers to be used in the categories GUI
* `back-slot`: Slot of the Go Back item in the categories GUI
* `products`: Lists out all the products for the category. More info [here](products.md)

Example:

```json
"categories": [
  {
    "title": "Example Category",
    "rows": 3,
    "slot": 13,
    "display-item": {
      "material": "BARRIER",
      "display": "Example Category"
    },
    "fillers": [
      0, 1, 2, 3, 4, 5, 6, 7, 8,
      9, 17,
      18, 19, 20, 21, 22, 23, 24, 25, 26
    ],
    "back_slot": 22,
    "products": []
  }
]
```

