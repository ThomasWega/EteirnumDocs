---
description: Displays a message to the player
---

# MSG

## **Parameters**:

* `type`: The type of message. List [here](msg.md#types)
* `msg`: The message to display.

### **Types:**

* `CHAT`
* `ACTION_BAR`
* `TITLE`
* `SUBTITLE`
* `TITLE_TIME`
  * additional `fade-in`, `stay`, `fade-out` settings

Example:

```json
"MSG": [
  {
    "type": "CHAT",
    "msg": "<yellow>You have activated the spell!"
  },
  {
    "type": "TITLE_TIME",
    "fade-in": 20,
    "stay": 20,
    "fade-out": 20
  }
]
```
