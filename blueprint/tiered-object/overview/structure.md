---
description: 'A typical blueprint is structured as follows:'
---

# Structure

```json
{
  "id": "unique_id",
  "impl": "IMPLEMENTATION_TYPE",
  "tiers": [
    {
      "item": {
        "material": "MATERIAL_TYPE",
        "display": "<color_code>Display Name",
        "lore": [
          "Item Description"
        ]
      },
      "effects": [
        // Define effects here
      ],
      // Additional attributes or settings
    }
  ]
}
```

### Components

* **ID**: A unique identifier for the blueprint. Multiple blueprints can have the same id, but only one id is allowed per Implementation Type
* **Implementation Type** (`impl`): Defines the type of item or action (e.g., `SPELL`, `POTION`, `GEAR`). New type cannot be defined unless it's hard-coded in.
  * Needs to be UPPER\_CASE
* [**Tiers**](../tiers.md): A list of tiers that define the item's characteristics. Each tier can have different properties, effects, and attributes. Implementation Types might handle these differently and provide more options

## Editing files

JSON is used everywhere. We recommend using VS Code with our formatting, which you can find download here

{% file src="../../.gitbook/assets/eteirnum_json.editorconfig" %}
formatting for JSON
{% endfile %}

We recommend following this [guide from Microsoft](https://learn.microsoft.com/en-us/visualstudio/ide/create-portable-custom-editor-options?view=vs-2022#add-and-remove-editorconfig-files).

## Folder Organization

Note that blueprints can be saved in any subdirectory of their main path. E.g `SPELL` blueprint used only for swords can be saved in the `sword` folder. These folders are optional and can be anything. All folders will be traversed when blueprints are being loaded.
