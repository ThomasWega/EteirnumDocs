---
description: Freeze the target
---

# FREEZE

## Parameters:

* `freeze-ticks`: how many ticks to freeze the target for
* `lock`: whether to prevent default vanilla freeze tick modifying freeze ticks
  * default is `true`

Example:

```json
"FREEZE": {
  "ignore-unapply": true,
  "target": "TARGET",
  "freeze-ticks": 60
}
```
