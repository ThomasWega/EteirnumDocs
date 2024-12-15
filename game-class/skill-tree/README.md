---
description: Progression paths with rewards at each step
---

# Skill Tree

Skill trees are grid-based systems where nodes, represented by unique characters, can be unlocked using skill points. Each node is linked to specific rewards or actions. Players spend skill points to unlock nodes, gaining the associated abilities or bonuses. Nodes may have prerequisites, creating a structured progression. In some cases, a node may offer multiple options, and players must choose only one of the available rewards or actions.

## Node Layout

The `nodes` section uses a grid of characters to represent the skill tree layout:

* Use `-` for empty spaces
* Use characters (A-Z, 0-9) for skill nodes
  * Each character must be unique across the entire grid
* Each row must have exactly 9 characters
* You can have up to 6 rows

Example:

```json
"nodes": [
  "-----6A--",
  "----FDE--",
  "-G3UTW---",
  "--JKL----",
  "-MNHI----",
  "-PY-Q----"
]
```

## **Node Bindings**

Each node in the `bindings` section can have the following properties:

* `skill-points`: Number of points required to unlock this node
* `initial` (optional): Set to `true` for first nodes to be unlocked on the tree
* `skills`: An array of skills available at this node. More info [here](skills/)

Example

```json
"K": {
  "initial": true,
  "skill-points": 1,
  "skills": [
    {
      "bind-id": "dusk_ward",
      "type": "SPELL",
      "spell-id": "dusk_ward",
      "tier": 0
    }
  ]
}
```

