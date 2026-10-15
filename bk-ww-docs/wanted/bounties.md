# Creating bounties

Open the **bounty registry** point with ox_target and go to **New bounty**.

<figure><img src="https://raw.githubusercontent.com/Boy4K/bk-ww-docs/main/assets/new-bounty.jpg" alt="New bounty with live poster preview"><figcaption><p>New bounty with live poster preview</p></figcaption></figure>

| Field | |
| --- | --- |
| Photo link | Fivemanage, Imgur, Discord… (allowed domains in `Config.Images`) |
| Name | the wanted person |
| Crimes / reason | optional, shown under the name |
| Bounty | between `MinBounty` and `MaxBounty` |
| Extra reward | optional free text (e.g. *2 gold bars*) |

The preview on the right is exactly what will be printed. Text that is too long shrinks to fit the poster.

## Active bounties

<figure><img src="https://raw.githubusercontent.com/Boy4K/bk-ww-docs/main/assets/board.jpg" alt="Active bounties: print, assign, cancel"><figcaption><p>Active bounties: print, assign, cancel</p></figcaption></figure>

Each card shows who created it, how many posters are printed and stuck, and when it expires.

| Button | |
| --- | --- |
| **Print** | choose the copies, you receive `wanted_poster` items |
| ✓ **Assign and close** | write who receives the bounty and optional notes |
| ⦸ **Cancel** | the creator or an admin |

{% hint style="info" %}
The script does **not** pay anyone: assigning only records who received the bounty. Payment is handled by your staff or police in RP.
{% endhint %}

When a bounty is assigned, cancelled or expires, its posters disappear from the walls (`RemoveOnClose`).
