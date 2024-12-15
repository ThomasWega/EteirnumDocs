---
description: Parameters that all Effect implementations have
---

# Shared Parameters

## **Parameters**:

* `target`: Target to apply the effect for. More info [here](target.md)
* `propagate`: Share modified effect parameters with other effects. More info [here](propagate.md)
* `ticks`: Tick interval between effect activations. More info [here](ticks.md)
* `repeat`: Amount of times to repeat the effect. More info [here](repeat.md)
* `stop-on-death`: If true, the effect will stop when the target dies. More info [here](stop-on-death.md)
* `ignore-apply`: If true, the effect will ignore the apply phase. More info [here](ignore-apply.md)
* `ignore-unapply`: If true, the effect will ignore the unapply phase. More info [here](ignore-unapply.md)

{% hint style="warning" %}
When modifying the [Shared Parameters](./), take caution of [Propagate](propagate.md) toggle
{% endhint %}
