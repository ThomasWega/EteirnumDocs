---
description: Attributes present on a player and their handling
---

# Overview

## Base and Bonus values

Some attributes have `BASE` values variants. How this works is, that the base values stays the same and is only changed on certain actions like level up.

Non base values on the other hand act as kind of a bonus value. These might be updated while holding items, having consumed potions, applying skills etc.

The calculations are simple. Total attribute value is calculated like so:

$$
\text{totalAttributeValue} = \text{baseAttributeValue} + \text{attributeValue}
$$

## Modifying attributes

{% hint style="warning" %}
When modyfing attributes, for example with [Blueprint](https://app.gitbook.com/o/y2atbaFomvwTmsuxAKt7/s/PEypf6i3dQewsaETmwpg/), you most likely don't want to modify the [Base values](./#base-values).
{% endhint %}

## Displayed values

some attribute types can display the value differently, than actually handled internally and in formulas. Here is a list of calculations made between the internal and displayed values. If an attribute type is listed here, it also includes it's [base type](./#base-values) (if it has any).&#x20;

If the attribute type is not listed here, it's display value is the same it's internal one. Please note that other things may change display values. E.g [ATTRIBUTE\_MODIFIER](https://app.gitbook.com/s/PEypf6i3dQewsaETmwpg/tiered-object/effects/implementations/attribute_modifier "mention")

* [`HP_REGEN_TICKS`](player-attributes/hp_regen_ticks.md) - $$\frac{N}{20}$$
* [`MANA_REGEN_TICKS`](player-attributes/mana_regen_ticks.md) - $$\frac{N}{20}$$
* [`SPEED`](player-attributes/speed.md) - $$N \times 100$$
