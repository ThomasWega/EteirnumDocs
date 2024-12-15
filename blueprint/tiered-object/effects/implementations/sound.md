---
description: Plays a sound effect
---

# SOUND

## **Parameters**:

* `sound`: The sound to play. Full string representation
* `volume`: The volume of the sound
  * from `0.0` to `1.0`
  * default is `1.0`
* `pitch`: The pitch of the sound
  * from `0.5` to `2.0`
  * default is `1.0`

{% hint style="success" %}
[Viewers parameter](../#viewable-effects) supported
{% endhint %}

Example:

```json
"SOUND": {
  "sound": "entity.player.attack.sweep",
  "volume": 0.5,
  "pitch": 0.5
}
```
