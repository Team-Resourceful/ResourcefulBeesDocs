# **Spawn Data**

## **Enabling Natural Spawns**
***


### **canSpawnInWorld** (Required)

`canSpawnInWorld`  must be set to `true` when you want bees to spawn in the world naturally.

<br>
<br>

### **Biome Whitelist && Biome Blacklist** (Optional)

These values are *optional.* The values are comma-separated and used in combination with the `canSpawnInWorld` value. This value can be expressed in a variety of ways and as such the values are used to determine the dimension a bee may spawn in as well. It is much easier to show examples of their usage.

*Note:* You can use either [biome type tags](https://github.com/Dungeon-Derps-Development/ResourcefulBees/wiki/Biome-Tags) or specific biomes, you cannot use both simultaneously.
*** LINK WILL BE UPDATED SOON!! ***

This example will let the bee spawn in any nether biome.
```json
"spawnInWorld": true,
"biomeWhitelist": "tag:nether"
```
<br>

This example will let the bee spawn in any overworld biome except ocean biomes.
```json
"spawnInWorld": true,
"biomeWhitelist": "tag:overworld"
"biomeBlacklist": "tag:ocean"
```
<br>

This example will let the bee spawn in any mountain or hills biome except the desert hills biome.
```json
"spawnInWorld": true,
"biomeWhitelist": "TAG:Mountain, HILLS"
"biomeBlacklist": "minecraft:desert_hills"
```
<br>

This example will let the bee spawn in plains, frozen river, or beach biomes only.
```json
"spawnInWorld": true,
"biomeList": "minecraft:plains,minecraft:frozen_river,minecraft:beach"
```
<br>

*Note:* Take notice that letter casing and spaces have no impact on the bee's ability to spawn. However, when using a biome type tag, the prefix "tag:" **must** be included. <br>

*SPECIAL NOTE:* As of 1.15.2-0.2.4a, nests will generate in the biomes where bees are set to spawn. During generation a nest may randomly spawn additional bees consisting only of the bees allowed to spawn in the biome where the nest generated.

<br>
<br>
<!--stackedit_data:
eyJoaXN0b3J5IjpbODQxOTQzMTU0LDE5Mjg5NTcyMDcsMTY4ND
YzMzA3MV19
-->