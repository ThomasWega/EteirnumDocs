---
description: 'A typical Shop structure is as follows:'
---

# Structure

```json
{
  "id": "example_shop_menu",
  "title": "Example Shop",
  "rows": 3,
  "fillers": [],
  "categories": []
}
```

### Components

* **ID**: A unique name for the shop. The `id` is used to reference the shop within the game’s systems.
  * <mark style="color:orange;">The</mark> <mark style="color:orange;"></mark><mark style="color:orange;">`id`</mark> <mark style="color:orange;"></mark><mark style="color:orange;">must be unique across all shops to prevent conflicts.</mark>
  * It serves as the primary key for identifying the shops in the game’s logic.
* **Title**: A title of the shop
* **Rows**: How many rows the inventory has. Will be used in the GUI with categories
* **Fillers**: Slots in the GUI where filler items will be applied. Will be used in the GUI with categories
* **Categories**: Multiple or one category for the shop. More info [here](../categories.md)
