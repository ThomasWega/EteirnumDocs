---
description: Entities in certain range radius
---

# IN\_RANGE

## **Parameters**:

* `radius`: Radius the entities are inside of from the location
* `entity-limit`: Limit the amount of entities to apply the effects for
  * default is `no limit`
* `ignore-invoker`: Don't include the effect invoker inside the picked up entities
  * default is `false`
* `effects`: Effects to execute when the event is called\


## Placeholders:

<table><thead><tr><th>Placeholder</th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><code>%in_range_entity_count%</code></td><td>How many entities were picked up in the range</td><td></td></tr><tr><td><code>%in_range_entity_index%</code></td><td>The index of the current entity (new target). Starting from <code>0</code></td><td></td></tr></tbody></table>

Example:

<pre class="language-json"><code class="lang-json">"IN_RANGE": {
<strong>  "ignore-invoker": true,
</strong>  "radius": 3,
  "entity-limit": 3,
  "effects": [
    {
      "MSG": {
        "type": "CHAT",
        "msg": "&#x3C;yellow>You have attacked with Decimation!"
      }
    }
  ]
}
</code></pre>
