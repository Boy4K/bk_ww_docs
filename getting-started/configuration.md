# Configuration

Everything is set in **`config.lua`**. The only thing changed from the game is the [style](../posters/styles.md) of posters and front pages.

## General

```lua
Config.Locale        = 'it'        -- 'it' or 'en' (files in locales/)
Config.Currency      = '$'
Config.AdminGroups   = { 'owner', 'admin', 'mod', 'superadmin' }
Config.AdminCommand  = 'bkww'      -- opens the panel anywhere (admins)
Config.CoordsCommand = 'bkww_coords'
Config.Webhook       = ''          -- Discord log, empty = off
Config.HistoryDays   = 30          -- closed bounties and archived articles are deleted after X days (0 = never)
```

## Registry points

Where jobs open the panel with ox_target.

```lua
Config.Points = {
    { type = 'wanted', label = 'Bounty registry', coords = vec3(441.20, -981.50, 30.70) },
    { type = 'news',   label = 'Newsroom',        coords = vec3(-598.10, -929.90, 23.90) },
}
```

| type | Opens | For |
| --- | --- | --- |
| `wanted` | Bounty registry | jobs in `Config.Wanted.Jobs` |
| `news` | Newsroom | jobs in `Config.News.Jobs` |

{% hint style="info" %}
Stand in front of the desk or PC and type `/bkww_coords`: a ready-to-paste `coords = vec3(...)` line appears in the F8 console.
{% endhint %}

## Wanted

```lua
Config.Wanted = {
    Enabled    = true,
    Jobs       = { { name = 'police', grade = 0 }, { name = 'sheriff', grade = 0 } },
    MinBounty  = 500,
    MaxBounty  = 1000000,
    ExpireDays = 7,              -- 0 = never
    Subtitle   = '',             -- text under WANTED, empty = language default
    Item       = 'wanted_poster',
}
```

## News

```lua
Config.News = {
    Enabled    = true,
    Name       = 'City Herald',  -- newspaper name
    Jobs       = { { name = 'reporter', grade = 0, editor = 3 } },
    Approval   = true,           -- articles must be approved by an editor
    PosterItem = 'news_poster',
    PaperItem  = 'newspaper',
}
```

| Field | Meaning |
| --- | --- |
| `grade` | minimum grade to **write** articles |
| `editor` | minimum grade of the **editor**: approves, rejects, archives, deletes |

## Posters on walls

```lua
Config.Posters = {
    PrintMax          = 10,     -- copies per print
    MaxPosters        = 150,    -- posters + front pages in the whole city
    Hours             = 48,     -- they fall off after X hours (0 = never)
    Scale             = 0.8,    -- max size (1.0 = 55 x 79 cm)
    DrawDistance      = 30.0,
    RemoveOnClose     = true,   -- removed when the bounty closes / the article is archived
    CitizensCanRemove = false,
}
```

## Images

```lua
Config.Images = {
    DomainCheck    = true,
    AllowedDomains = { 'fivemanage.com', 'cdn.discordapp.com', 'media.discordapp.net', 'i.imgur.com' },
}
```

{% hint style="warning" %}
Discord attachment links expire after about a day. For posters that must last, use Fivemanage or Imgur.
{% endhint %}

Restart the resource after changing `config.lua`.
