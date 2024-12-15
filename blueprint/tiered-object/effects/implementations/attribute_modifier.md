---
description: Modifies player attributes
---

# ATTRIBUTE\_MODIFIER

## **Parameters**:

* `modifier`: Data for the modifier
  * `attribute`: The attribute to modify. List [here](https://app.gitbook.com/s/jhq5tF3c6kQlOG37iBdD/player-attributes)
  * `range`: Number range
    * only range in [`RANDOM`](attribute_modifier.md#type) type supports [Placeholders](../#placeholders)
  * `logic`: The logic type. More info [here](attribute_modifier.md#logic)
    * default is `FLAT`
  * `display`: How the modification is displayed. More info [here](attribute_modifier.md#display)
    * default is `NONE`
  * `type`: The modification type (e.g., `STATIC`, `RANDOM`). More info [here](attribute_modifier.md#type)

### Logic

Determines how the math will be calculated on the range.

* `PERCENTAGE`
  * in decimal (0.08 = 8% increase)
* `FLAT`
  * in points. (12 = +12 HP)
* `MULTIPLIER`
  * in decimal (0.1 = 0.1x multiplier)

### Display

Determines how the attribute will be shown.

* `NONE`
* `SECONDS`
  * `s` will be inserted after number
* `PERCENTAGE`
  * number will be multiplied by 100
  * `%` will be inserted after number

### Type

There are currently only two types. For a new one to be added, it needs to be hard coded

* `STATIC`
  * sets a static value from the range
  * is applied only once object generation and stays forever
  * e.g `range[10, 20]` can be set to 12 or 14 or 16 etc.
* `RANDOM`
  * keeps the range
  * on object activation/usage gets a random number from the range each time

Example:

```json
"ATTRIBUTE_MODIFIER": {
  "ticks": [0, 320],
  "modifier": {
    "attribute": "ATTACK_DAMAGE",
    "range": 1,
    "logic": "MULTIPLIER",
    "display": "NONE",
    "type": "STATIC"
  }
}
```
