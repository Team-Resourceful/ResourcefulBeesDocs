This page contains a template for the bee jsons with ALL configurable options. This should help pack devs with making their own bees since fields only need to be modified or deleted as necessary.

```json
{ 
	"flower":"ALL",
	"baseLayerTexture":"/creeper/creeper_bee",
	"maxTimeInHive":600,
	"attackDamage":4.0,
	"sizeModifier":1.5,
	"traits":["wither","blaze","canswim","creeper","zombie","pigman","ender","nether"],
	"hasHoneycomb":true,
	"ColorData": {
		"primaryColor":"#005500",
		"secondaryColor":"#005500",
		"honeycombColor":"#005500",
		"primaryLayerTexture":"/custom/primary_layer",
		"secondaryLayerTexture":"/custom/secondary_layer",
		"emissiveLayerTexture":"/creeper/creeper_bee_emissive",
		"isBeeColored": true,
		"isRainbowBee": false,
		"isGlowing" : true,
		"glowColor" : "#55ff55",
		"isEnchanted" : false,
		"glowingPulse" : 2
	},
	"MutationData": {
		"hasMutation":true,
		"mutationInput" : "minecraft:stone",
		"mutationOutput":"minecraft:water",
		"mutationCount":6,
		"mutationType":"BLOCK_TO_FLUID"
	},
	"CentrifugeData": {
		"hasCentrifugeOutput": true,
		"mainOutput":"minecraft:stone",
		"secondaryOutput":"minecraft:diamond",
		"bottleOutput":"minecraft:dragons_breath",
		"mainOutputWeight":0.9,
		"secondaryOutputWeight":0.5,
		"bottleOutputWeight":0.25,
		"mainOutputCount":1,
		"secondaryOutputCount":2,
		"bottleOutputCount":4,
		"mainInputCount":4
	},
	"SpawnData": {
		"canSpawnInWorld":true,
		"spawnWeight": 8,
		"biomeWhitelist":"tag:ocean",
		"biomeBlacklist":"tag:overworld",
		"minGroupSize": 1,
		"maxGroupSize": 1,
		"lightLevel": "ANY"
	},
	"BreedData": {
		"isBreedable": true,
		"breedWeight": 2.5,
		"parent1": "testbeeparent1",
		"parent2": "testbeeparent2",
		"feedItem":
		"minecraft:poppy",
		"feedAmount": 5
	},
	"TraitData": {
		"hasTraits": true
	}
	}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEwNjYzODg3ODJdfQ==
-->