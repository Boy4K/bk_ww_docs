# Inventory items

Add these to `ox_inventory/data/items.lua`:

```lua
['wanted_poster'] = {
    label = 'WANTED poster',
    weight = 20, stack = true, close = true,
    client = { export = 'bk_ww.usePoster' }
},
['news_poster'] = {
    label = 'Front page',
    weight = 20, stack = true, close = true,
    client = { export = 'bk_ww.usePoster' }
},
['newspaper'] = {
    label = 'Newspaper',
    weight = 50, stack = true, close = true,
    client = { export = 'bk_ww.readNewspaper' }
},
```

| Item | Used for |
| --- | --- |
| `wanted_poster` | Stick a WANTED poster on a wall |
| `news_poster` | Stick a front page on a wall |
| `newspaper` | Read the full article from the inventory (can be given to other players) |

Every printed copy carries its data in the metadata: the inventory shows the name, the amount or headline, and the photo.

{% hint style="warning" %}
The item names must match `Config.Wanted.Item`, `Config.News.PosterItem` and `Config.News.PaperItem`. If another script already uses one of these names, rename it in both places.
{% endhint %}
