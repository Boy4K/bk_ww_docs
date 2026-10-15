---
description: Bounties and a newspaper for your city — printed, posted on walls, read in game.
cover: https://raw.githubusercontent.com/Boy4K/bk-ww-docs/main/assets/cover.png
coverY: 0
---

# BK Wanted & News

BK Wanted & News puts two things in one resource:

* **Wanted** — the police create bounties with a photo and a reward, print WANTED posters and stick them on any wall.
* **News** — reporters write articles with headline, photo and body. The editor approves them, then they go on walls as front pages or into players' hands as newspapers.

Citizens never open a panel: they only see what is posted around town and read it with ox_target. **Posters stay on the walls after restarts.**

<figure><img src="https://raw.githubusercontent.com/Boy4K/bk-ww-docs/main/assets/in-game.jpg" alt="A WANTED poster stuck on a wall in game"><figcaption><p>A WANTED poster stuck on a wall in game</p></figcaption></figure>

## What's inside

| Area | What you get |
| --- | --- |
| **Bounties** | Photo from a link, name, crimes, amount and extra reward · active bounties board · registry with full history · manual assignment with notes · automatic expiry |
| **Newspaper** | Article editor with live front-page preview · drafts · editor approval with rejection notes · archive |
| **Printing** | WANTED posters, front pages for walls, newspapers to read from the inventory — all as ox_inventory items with metadata |
| **Walls** | Live preview where you aim · mouse wheel to resize · tear down with animation · hours on walls · city limit |
| **Styles** | 3 WANTED styles + 3 front-page styles, chosen from the panel and applied instantly |
| **Config** | Everything else in `config.lua`: language, jobs and grades, points, amounts, items |
| **Extras** | Discord logs · Italian and English · exports and events for other scripts |

## Requirements

| Resource | Needed |
| --- | --- |
| es\_extended **or** qb-core | yes |
| oxmysql | yes |
| ox\_inventory | yes |
| ox\_target | recommended (without it: `E` / `G` keys) |
| ox\_lib | optional (notifications) |

{% hint style="success" %}
No SQL to import: the tables are created automatically when the resource starts. See [Installation](getting-started/installation.md).
{% endhint %}
