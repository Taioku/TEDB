# first we get @s data
```mcfunction
function tedb:api/get
```

# we write our data on tedb:io player.data
```mcfunction
data modify storage tedb:io player.data.Inventory set from entity @s Inventory
```
```mcfunction
data modify storage tedb:io player.data.EnderItems set from entity @s EnderItems
```
```mcfunction
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

# erase data by saving empty player.data
```mcfunction
function tedb:api/get
```
```mcfunction
data remove storage tedb:io player.data.CustomData
```
```mcfunction
function tedb:api/save
```