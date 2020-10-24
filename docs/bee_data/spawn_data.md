# **Spawn Data**

## **Enabling Natural Spawns**
***


### **canSpawnInWorld** (Required)

`canSpawnInWorld` must be set to `true` when you want bees to spawn in the world naturally. This means they spawn in the same manner as other passive mobs.

<br>
<br>

### **Biome Whitelist && Biome Blacklist** (Optional)

These values are *optional.* The values are comma-separated and used in combination with the `canSpawnInWorld` value. This value can be expressed in a variety of ways and as such the values are used to determine the dimension a bee may spawn in as well. It is much easier to show examples of their usage.

*Note:* You can use either [biome type tags](https://github.com/Dungeon-Derps-Development/ResourcefulBees/wiki/Biome-Tags) or specific biomes, you cannot use both simultaneously.
*** LINK WILL BE UPDATED SOON!! ***

This example will let the bee spawn in any nether biome.
```json
"SpawnData": {
	"canSpawnInWorld": true,
	"biomeWhitelist": "tag:nether"
}
```
<br>

This example will let the bee spawn in any overworld biome except ocean biomes.
```json
"SpawnData": {
	"canSpawnInWorld": true,
	"biomeWhitelist": "tag:overworld"
	"biomeBlacklist": "tag:ocean"
}
```
<br>

This example will let the bee spawn in any mountain or hills biome except the desert hills biome.
```json
"SpawnData": {
	"canSpawnInWorld": true,
	"biomeWhitelist": "TAG:Mountain, HILLS"
	"biomeBlacklist": "minecraft:desert_hills"
}
```
<br>

This example will let the bee spawn in plains, frozen river, or beach biomes only.
```json
"SpawnData": {
	"canSpawnInWorld": true,
	"biomeList": "minecraft:plains,minecraft:frozen_river,minecraft:beach"
}
```
<br>

**SPECIAL NOTE:** Nests will generate in the biomes where bees are set to spawn. During generation a nest may come preloaded with additional bees consisting only of the bees *allowed* to spawn in the biome where the nest generated. Nest generation can be disabled by setting the global config value `generateBeeNests` to `false`.

<br>
<br>


<!--stackedit_data:
eyJoaXN0b3J5IjpbMTI1OTY0MjY4OCwxOTI4OTU3MjA3LDE2OD
Q2MzMwNzFdfQ==
-->