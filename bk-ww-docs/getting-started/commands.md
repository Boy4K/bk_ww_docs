# Commands and permissions

| Command | Who | What |
| --- | --- | --- |
| `/bkww` | admins | Opens the panel anywhere |
| `/bkww_coords` | admins | Prints coordinates for `Config.Points` in F8 |
| `/bkww_debug` | everyone | Shows job, grade and permissions — useful when a point doesn't open |

Command names can be changed in `config.lua`.

## Who sees what

| Role | How | Sees |
| --- | --- | --- |
| **Admin** | group in `Config.AdminGroups` | everything + **Styles** |
| **Police** | job in `Config.Wanted.Jobs` | Active bounties, New bounty, Registry |
| **Reporter** | job in `Config.News.Jobs`, grade ≥ `grade` | Newsroom, New article (own drafts) |
| **Editor** | same job, grade ≥ `editor` | + every draft, approve, reject, archive, delete |
| **Citizen** | anyone | posters and front pages on walls, newspapers in hand |

Permissions are checked on the server, the same way when the target option is shown and when the panel opens.
