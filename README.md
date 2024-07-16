# first we get @s data
```mcfunction
function tedb:api/get
```

# we write our data on tedb:io player.data
```mcfunction
data modify storage tedb:io player.data.Inventory set from entity @s Inventory
data modify storage tedb:io player.data.EnderItems set from entity @s EnderItems
data modify storage tedb:io player.data.CustomData set value "Custom Data!"
```

# we save our data
```mcfunction
function tedb:api/save
```

# we clean cache
```mcfunction
data remove storage tedb:io player
```