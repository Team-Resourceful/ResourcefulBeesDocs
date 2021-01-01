# **Spawn Data**

## **Enabling Natural Spawns**
***


### **canSpawnInWorld** (Required)

`canSpawnInWorld` must be set to `true` when you want bees to spawn in the world naturally. This means they spawn in the same manner as other passive mobs.

<br>
<br>

### **Biome Whitelist && Biome Blacklist** (Optional)

These values are *optional.* The values are comma-separated and used in combination with the `canSpawnInWorld` value. This value can be expressed in a variety of ways and as such the values are used to determine the dimension a bee may spawn in as well. It is much easier to show examples of their usage.

*Note: You can use either* [biome type tags](https://resourceful-bees.readthedocs.io/en/1.16.3/extra_stuff/biome_tags/) *or specific biomes, you cannot use both simultaneously.*

This example will let the bee spawn in any nether biome.
```json
"SpawnData": {
	"canSpawnInWorld": true,
	"biomeWhitelist": "tag:nether"
}
```
<br>

This example will let the bee spawn in any overworld biome except ocean biomes. (Default Implementation)
```json
"SpawnData": {
	"canSpawnInWorld": true,
	"biomeWhitelist": "tag:overworld",
	"biomeBlacklist": "tag:ocean"
}
```
<br>

This example will let the bee spawn in any mountain or hills biome except the desert hills biome.
```json
"SpawnData": {
	"canSpawnInWorld": true,
	"biomeWhitelist": "TAG:Mountain, HILLS",
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

## **Strength in Numbers**
***

### **spawnWeight** (Optional)

`spawnWeight` is an integer value which represents the weighting of the bee against all other entities registered to spawn in the biomes where the bee can spawn. The value is **not** a percent representation meaning any value greater than zero can be used here. By default the value is set as `8` which puts the weighting just below chickens and pigs which are set at `10`.

_Note: Because this value determines the weight of the entity spawn against all other entities, this means the bee will have a 100% chance to spawn when it is the_ **only** _entity registered to spawn in the biome._

This example will let the bee spawn in any mountain or hills biome except the desert hills biome with a weight of **two**.
```json
"SpawnData": {
	"canSpawnInWorld": true,
	"biomeWhitelist": "TAG:Mountain, HILLS",
	"biomeBlacklist": "minecraft:desert_hills",
	"spawnWeight": 2
}
```

<br>
<br>

### **Group Sizes** (Optional)

`minGroupSize` and `maxGroupSize` determine the minimum and maximum number of bees which will spawn at once. By default these values are set to `0` and `3`, respectively.

This example will let only a single bee spawn in any mountain or hills biome except the desert hills biome with a weight of **two**.
```json
"SpawnData": {
	"canSpawnInWorld": true,
	"biomeWhitelist": "TAG:Mountain, HILLS",
	"biomeBlacklist": "minecraft:desert_hills",
	"spawnWeight": 2,
	"minGroupSize": 1,
	"maxGroupSize": 1
}
```

<br>
<br>

## **Additional Options**
***

### **lightLevel** (Optional)

`lightLevel` is slightly misleading in terms of the value options. Currently, only three options are available for `lightLevel`: `DAY`, `NIGHT`and `ANY`.

`DAY` = light levels of `8+`
`NIGHT` = light levels of `7-`
`ANY` = any light level

As of now, this value only controls the light level a block must be at for the bee to spawn. It is *not* representative of the daylight cycle as it may seem on first glance. *In a future update* we will be using this value to force bees to only work during specific times of day.

**SPECIAL NOTE:** This value also affects breeding. When the bee is set as breedable, it will only spawn the child if the light level of the block at the time is the correct light level.

<br>
<br>

## **Template**
***

Here is a template for all configurable options in the Spawn Data Object:

```json
"SpawnData": {
	"canSpawnInWorld": true,
	"biomeWhitelist": "TAG:Mountain, HILLS",
	"biomeBlacklist": "minecraft:desert_hills",
	"spawnWeight": 2,
	"minGroupSize": 1,
	"maxGroupSize": 1,
	"lightLevel": "ANY"
}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbNzU0Nzc3MjQyLC0xOTIxMTgxOTYzLDE5Mj
g5NTcyMDcsMTY4NDYzMzA3MV19
-->