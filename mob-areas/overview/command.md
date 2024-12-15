# Command

To manage the mob area, use:

```
/adminmobspawn area add <areaName> <world> <pos1> <pos2>
/adminmobspawn area remove <areaName>
/adminmobspawn area list
/adminmobspawn area reload
/adminmobspawn area saveAll
```

To manage the config of a specific area, use:

```
/adminmobspawn area config mobs add <areaName> <mobName>
/adminmobspawn area config mobs remove <areaName> <mobName>
/adminmobspawn area config mobs list <areaName>

/adminmobspawn area config groups add <areaName> <groupName> <minMobs> <maxMobs> <mobs>
/adminmobspawn area config groups remove <areaName> <groupName>
/adminmobspawn area config groups list <areaName>
```

{% hint style="warning" %}
Do note that only some of the settings are changeable with the commands. Everything can be changed manually in the data file though
{% endhint %}
