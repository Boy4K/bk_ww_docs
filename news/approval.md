# Editor approval

<figure><img src="../assets/newsroom.jpg" alt="The newsroom: drafts, pending, published, archived"><figcaption><p>The newsroom: drafts, pending, published, archived</p></figcaption></figure>

Editors (grade ≥ `editor` in `Config.News.Jobs`) see every article.

| Status | What editors can do |
| --- | --- |
| **Pending** | ✓ approve and publish · ✕ reject with a note · edit |
| **Draft** | edit · delete |
| **Published** | print · archive · delete |
| **Archived** | delete |

## Rejecting

<figure><img src="../assets/reject.jpg" alt="Rejecting with a note for the reporter"><figcaption><p>Rejecting with a note for the reporter</p></figcaption></figure>

The article goes back to drafts and the reporter sees the note at the top of the editor.

## Archive

Archiving stops printing and (with `RemoveOnClose`) takes its front pages off the walls. **Clear archive** deletes every archived article; `Config.HistoryDays` does it automatically.
