# Female Starter Pack Script | BJ Development

Framework Compatibility: ESX & QBCore
Inventory Required: ox_inventory (v2.40.2 or newer)

This script adds a Female Starter Pack item to your server, giving new female characters a convenient set of starting items. It also includes Discord webhook logging for tracking usage. Fully compatible with ESX and QBCore frameworks.

Features

Adds a female_starterpack item to your server.

Fully compatible with ESX & QBCore.

Works with ox_inventory v2.40.2+.

Sends usage logs to Discord via webhook.

Designed for serious RP servers.

ESX Installation

Open es_extended/config.lua and add/update your starter inventory:

Config.StartingInventoryItems = {
    female_starterpack = 1,
}


Add the item to ox_inventory/data/items.lua:

["female_starterpack"] = {
    label = "Female Starter Pack",
    weight = 3,
    stack = true,
    close = false,
    description = "Female Starter Pack",
    client = {
        image = "female_starterpack.png",
    }
},


Restart your server.

QBCore Installation

Open qb-core/shared/main.lua and add the starter item:

QBShared.StarterItems = {
    ['female_starterpack'] = { amount = 1, item = 'starter_pack' },
}


Add the item to qb-core/shared/items.lua:

female_starterpack = { 
    name = 'female_starterpack', 
    label = 'Female Starter Pack', 
    weight = 300, 
    type = 'item', 
    image = 'female_starterpack.png', 
    unique = true, 
    useable = true, 
    shouldClose = false, 
    description = "Female Starter Pack" 
},


Restart your server.

Notes

Ensure female_starterpack.png exists in your inventory images folder.

Compatible with serious RP servers to give female characters a starting set of items efficiently.

Discord webhook logging can be configured for tracking starter pack usage.
