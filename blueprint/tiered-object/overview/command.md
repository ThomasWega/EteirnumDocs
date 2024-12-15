---
description: List of possible commands for blueprint
---

# Command

These are shared commands between all of the implementations:

```
/admin{implementation} reload
```

To give the display item, use:

```
/admin{implementation} give <id> <tier> <player>
```

Example:

```
/adminspell reload
```

## SPELL

These are commands only for the [SPELL implementation](../implementations/spell.md).

To test the spell in game use:

```
/adminspell test <id> <tier> <skills>
```

To open a custom GUI to bind a spell to right-left click combination use:

```
/adminspell bind <id>
```

To set the skill as owned to a player, use the command:

```
/adminspell set <id> <tier> <skills>
```

To see list of owned spells of a player use:

```
/adminspell list <player>
```

To remove all the currently active spells from a player, use:

```
/adminspell clear <player>
```
