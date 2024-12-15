---
description: 'A typical Game Class is structured as follows:'
---

# Structure

```json
{
  "id": "unique_id",
  "default-class": true/false,
  "display-name": "Class Name",
  "description": [
    "Brief description of the class."
  ],
  "icon": "ICON_TYPE",
  "skill-tree": {
    "nodes": [
      "Skill tree layout"
    ],
    "bindings": {
      // Define bindings here
    }
  }
}

```

### Components

* **ID**: A unique identifier for the game class. The `id` is used to reference the class within the game’s systems.
  * <mark style="color:orange;">The</mark> <mark style="color:orange;"></mark><mark style="color:orange;">`id`</mark> <mark style="color:orange;"></mark><mark style="color:orange;">must be unique across all classes to prevent conflicts.</mark>
  * It serves as the primary key for identifying the class in the game’s logic.
* **Default Class**: A boolean value that determines if this class is the default starting class for new players.
  * <mark style="color:orange;">Only one class can have</mark> <mark style="color:orange;"></mark><mark style="color:orange;">`default-class`</mark> <mark style="color:orange;"></mark><mark style="color:orange;">set to</mark> <mark style="color:orange;"></mark><mark style="color:orange;">`true`</mark><mark style="color:orange;">.</mark>
* **Display Name**: The human-readable name of the class, which is shown to players in certain GUIs
* **Description**: Fairly short description of the class shown to the players in certain GUIs
* **Icon**: Represents the visual icon. Shown to players in certain GUIs
  * Should be `UPPER_CASE`
* **Skill Tree**: Progression of abilities and spells. More info [here](../skill-tree/)
