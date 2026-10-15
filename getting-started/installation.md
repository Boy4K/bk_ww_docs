# Installation

{% stepper %}
{% step %}
### Copy the resource

Put the `bk_ww` folder in your `resources` folder.
{% endstep %}

{% step %}
### Add the inventory items

Add the three items from [Inventory items](inventory-items.md) to `ox_inventory/data/items.lua`.
{% endstep %}

{% step %}
### Start order

In `server.cfg`, start it **after** its dependencies:

```
ensure oxmysql
ensure es_extended   # or qb-core
ensure ox_inventory
ensure ox_target
ensure bk_ww
```
{% endstep %}

{% step %}
### Set up config.lua

Set language, jobs, grades and the registry points. See [Configuration](configuration.md).
{% endstep %}

{% step %}
### Start the server

The resource creates its own database tables on start. Nothing to import.
{% endstep %}
{% endstepper %}

## Where things are saved

| Where | What |
| --- | --- |
| `bk_wanted_bounties` | bounties and their history |
| `bk_wanted_news` | articles (drafts, pending, published, archived) |
| `bk_wanted_posters` | WANTED posters and front pages stuck on walls |
| `data/styles.json` | the styles chosen from the panel |

{% hint style="info" %}
Updating from the older `bk_wanted` resource keeps every bounty, article and poster: the table names did not change.
{% endhint %}
