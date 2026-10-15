# Exports and events

All exports are **server-side**.

## CreateBounty

Same checks as the panel (allowed image domains, min/max amount).

```lua
local id, err = exports.bk_ww:CreateBounty({
    name   = 'John Doe',
    reason = 'Armed robbery',               -- optional
    image  = 'https://r2.fivemanage.com/....png',
    bounty = 25000,
    reward = '2 gold bars',                 -- optional
}, source)  -- creator: player source, a table { name, job, identifier } or nil (= "System")
```

## CloseBounty / CancelBounty

```lua
local ok, err = exports.bk_ww:CloseBounty(id, 'Tony Rossi', 'Paid in cash', 'Officer Bianchi')
local ok, err = exports.bk_ww:CancelBounty(id, 'Admin')
```

## Reading bounties

```lua
local bounty = exports.bk_ww:GetBounty(id)          -- any status, nil if not found
local list   = exports.bk_ww:GetActiveBounties()    -- highest first
local wanted, bounty = exports.bk_ww:IsWanted('John Doe')   -- exact name, case-insensitive
```

## Events

```lua
AddEventHandler('bk_ww:bountyCreated', function(bounty) end)
AddEventHandler('bk_ww:bountyClosed', function(bounty)
    -- bounty.status = 'claimed' | 'cancelled' | 'expired'
end)
```

## Bounty object

| Field | Type |
| --- | --- |
| `id`, `bounty`, `printed`, `posters` | number |
| `name`, `reason`, `image`, `reward`, `status` | string |
| `creator_name`, `creator_job`, `assigned_to`, `note`, `closed_by_name` | string |
| `created`, `closed`, `expires` | unix timestamp |
