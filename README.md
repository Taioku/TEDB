```mcfunction
# first we get @s data
function tedb:api/get

# we write our data on tedb:io player.data
data modify storage tedb:io player.data.Inventory set from entity @s Inventory
data modify storage tedb:io player.data.EnderItems set from entity @s EnderItems
data modify storage tedb:io player.data.CustomData set value "Custom Data!"

# we save our data
function tedb:api/save

# we clean cache
data remove storage tedb:io player
```