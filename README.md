# TreeRM -- Server Command

A **7 Days to Die server console command** for removing items from a
player's inventory or from all players.

This command is useful for: - Admin moderation - Removing bugged or
duplicated items - Server balancing - Emergency cleanup of certain items

------------------------------------------------------------------------

## Command Syntax

``` bash
treerm <PlayerName|SteamID|EntityId> <Item> [Count|all] [Quality]
treerm all <Item> [Count|all] [Quality]
```

### Parameters

  Parameter                             Description
  ------------------------------------- ------------------------------------
  **PlayerName / SteamID / EntityId**   Target player
  **all**                               Targets every player on the server
  **Item**                              Internal item name
  **Count**                             Number of items to remove
  **all**                               Remove every matching item
  **Quality**                           Optional quality filter

------------------------------------------------------------------------

# Examples

### Remove 1 item (any quality)

``` bash
treerm Bob pistol
```

Removes **1 pistol** from Bob regardless of quality.

------------------------------------------------------------------------

### Remove multiple items

``` bash
treerm Bob pistol 2
```

Removes **2 pistols** from Bob.

------------------------------------------------------------------------

### Remove items with specific quality

``` bash
treerm Bob pistol 2 2
```

Removes **2 pistols of quality 2**.

------------------------------------------------------------------------

### Remove all items of a type

``` bash
treerm Bob pistol all
```

Removes **every pistol** from Bob.

------------------------------------------------------------------------

### Remove all items of a specific quality

``` bash
treerm Bob pistol all 5
```

Removes **all pistols of quality 5**.

------------------------------------------------------------------------

### Remove from all players

``` bash
treerm all pistol all
```

Removes **all pistols from every player on the server**.

------------------------------------------------------------------------

### Target a SteamID

``` bash
treerm Steam_76561198016034203 gunMGT0PipeMachineGun 2
```

Removes **2 Pipe Machine Guns** from the specified SteamID.

------------------------------------------------------------------------

# Notes

-   If **Quality is provided**, only that quality will be removed.
-   If **Quality is omitted**, all qualities will match.
-   `all` can be used instead of a number to remove **every matching
    item**.
-   Works with **Player Name**, **SteamID**, or **EntityId**.

------------------------------------------------------------------------

# Use Cases

-   Removing **duped items**
-   Server **admin moderation**
-   Cleaning up **exploit items**
-   Managing **economy balance**

------------------------------------------------------------------------

# Compatibility

Designed for **7 Days to Die dedicated servers** with custom server
commands.

------------------------------------------------------------------------

# License

Free to use and modify.
