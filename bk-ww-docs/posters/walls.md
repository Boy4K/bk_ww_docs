# Posters on walls

WANTED posters and front pages work the same way.

<figure><img src="https://raw.githubusercontent.com/Boy4K/bk-ww-docs/main/assets/in-game.jpg" alt="A poster on a wall"><figcaption><p>A poster on a wall</p></figcaption></figure>

## Sticking one

Use the item from the inventory:

| Key | Action |
| --- | --- |
| aim | choose the wall — a preview appears (red = not allowed) |
| mouse wheel | size from 40 % to 100 % of `Config.Posters.Scale` |
| `E` | stick it (short animation) |
| `BACKSPACE` | cancel |

The item is used up and the poster stays there for everyone, even after a restart.

## On the wall

With ox_target:

* **Look at the poster** / **Read the newspaper** — anyone.
* **Tear down** — the bounty's jobs for WANTED posters, the newspaper's jobs for front pages, admins always. With `CitizensCanRemove = true`, anyone. Tearing plays an animation and the sheet falls off.

Without ox_target the same actions use `E` and `G`.

## Limits

| Option | |
| --- | --- |
| `Hours` | posters fall off by themselves after X hours |
| `MaxPosters` | maximum in the whole city |
| `DrawDistance` | distance they are drawn at |
| `RemoveOnClose` | removed when the bounty closes or the article is archived |

At night posters are drawn darker so they don't glow.
