# FAQ and troubleshooting

<details>
<summary>I see the registry point but can't open it</summary>

Run `/bkww_debug`. The job name must match `Config.Wanted.Jobs` or `Config.News.Jobs` exactly, your grade must be high enough, and the point must have the right `type` (`wanted` or `news`).
</details>

<details>
<summary>"This sheet is blank…" or another script opens when using the item</summary>

Another resource uses the same item name. Rename the item in `items.lua` and in `config.lua`.
</details>

<details>
<summary>Using the item does nothing</summary>

The item needs `client = { export = 'bk_ww.usePoster' }` (posters and front pages) or `bk_ww.readNewspaper` (newspaper). Restart ox_inventory after editing `items.lua`.
</details>

<details>
<summary>The poster won't stick</summary>

Aim at a wall (not floor or ceiling), within 3.5 m. Check the city limit `MaxPosters` and that the bounty is still active / the article is still published.
</details>

<details>
<summary>The photo is missing on a poster</summary>

The link expired (Discord links last about a day) or its domain isn't in `Config.Images.AllowedDomains`.
</details>

<details>
<summary>Posters are too big</summary>

Lower `Config.Posters.Scale` and use the mouse wheel while sticking them.
</details>
