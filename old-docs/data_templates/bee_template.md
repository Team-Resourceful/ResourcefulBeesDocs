## **Template**
***

This page contains a template for the bee jsons with ALL configurable options. This should help pack devs with making their own bees since elements only need to be modified or deleted as necessary.
!!!template "Template"
	```json
	{
		"flower":"ALL",
		"baseLayerTexture":"/creeper/creeper_bee",
		"maxTimeInHive":2400,
		"sizeModifier":1.0,
		"traits":["wither","blaze","can_swim","creeper","zombie","pigman","ender","nether", "oreo", "kitten", "slimy", "desert"],
		"hasHoneycomb":true,
		"customCombDrop": "",
		"customCombBlockDrop": "",
		"apiaryOutputAmounts" : [1,2,3,4],
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
			"glowingPulse" : 2,
			"modelType": "DEFAULT"
		},
		"CombatData": {  
			"isPassive": false,  
			"removeStingerOnAttack": true,
			"inflictsPoison": true,
			"attackDamage": 1
		},
		"MutationData": {
			"hasMutation":true,
			"mutationInput" : "minecraft:stone",
			"mutationOutput":"minecraft:water",
			"mutationCount":10,
			"mutationType":"BLOCK_TO_FLUID",
			"mutations" : [
				{
		"type": "BLOCK_TO_BLOCK",
		"inputID": "tag:minecraft:sand",
		"outputs": [
		  {"outputID": "minecraft:white_stained_glass"},
		  {"outputID": "minecraft:orange_stained_glass"},
		  {"outputID": "minecraft:magenta_stained_glass"},
		  {"outputID": "minecraft:light_blue_stained_glass"},
		  {"outputID": "minecraft:yellow_stained_glass"},
		  {"outputID": "minecraft:lime_stained_glass"},
		  {"outputID": "minecraft:pink_stained_glass"},
		  {"outputID": "minecraft:gray_stained_glass"},
		  {"outputID": "minecraft:light_gray_stained_glass"},
		  {"outputID": "minecraft:cyan_stained_glass"},
		  {"outputID": "minecraft:purple_stained_glass"},
		  {"outputID": "minecraft:blue_stained_glass"},
		  {"outputID": "minecraft:brown_stained_glass"},
		  {"outputID": "minecraft:green_stained_glass"},
		  {"outputID": "minecraft:red_stained_glass"},
		  {"outputID": "minecraft:black_stained_glass"}
		]
	      },
				{
		"type": "BLOCK_TO_BLOCK",
		"inputID": "tag:forge:stone",
		"defaultWeight": 10,
		"cdefaultChance" : 0.75,
		"outputs": [
		  {"outputID": "minecraft:redstone_ore", "weight": 1, "chance": 0.25}
		  {"outputID": "minecraft:lapis_ore", "weight": 3, "chance": 0.40}
		]
	      },
	      {
		"type": "BLOCK_TO_BLOCK",
		"inputID": "minecraft:honey_block",
		"outputs": [
		  {"outputID": "minecraft:glass", "chance": 0.5}
		]
	      }
				{
		"type": "BLOCK_TO_ITEM",
		"inputID": "tag:forge:ores/diamond",
		"outputs": [
		  {
		    "outputID": "minecraft:potion",
		    "nbtData": {
		      "Potion": "resourcefulbees:calming"
		    }
		  }
		]
	      },
				{
		"type": "ENTITY_TO_ENTITY",
		"inputID": "entity:cow",
		"outputs": [
		  {
		    "outputID": "entity:mooshroom",
		    "nbtData": {
		      "Type": "brown"
		    }
		  }
		]
	      }
			]
		},
		"CentrifugeData": {
			"hasCentrifugeOutput": true,
			"mainOutput":"minecraft:stone",
			"secondaryOutput":"minecraft:diamond",
			"bottleOutput": "minecraft:potion",
			"mainOutputWeight":0.9,
			"secondaryOutputWeight":0.5,
			"bottleOutputWeight":0.25,
			"mainOutputCount":1,
			"secondaryOutputCount":2,
			"bottleOutputCount":4,
			"mainInputCount":4,
			"mainNBTData": {
				"display":{
					"Name": "{\"text\":\"A Stone\"}"
				}
			},
			"secondaryNBTData": {
				"display":{
					"Name": "{\"text\":\"Crystal Diamond\"}"
				}
			},
			"bottleNBTData" : {
				"Potion": "resourcefulbees:calming"
			},
			"recipeTime": 200,
			"hasFluidoutput": false
		},
		"SpawnData": {
			"canSpawnInWorld":true,
			"spawnWeight": 8,
			"biomeWhitelist":"tag:ocean",
			"biomeBlacklist":"tag:overworld",
			"minYLevel": 0,
			"maxYLevel": 255,
			"minGroupSize": 1,
			"maxGroupSize": 1,
			"lightLevel": "ANY"
		},
		"BreedData": {
			"isBreedable": true,
			"breedWeight": 2.5,
			"breedChance": 0.1,
			"parent1": "testbeeparent1",
			"parent2": "testbeeparent2",
			"feedItem": "minecraft:poppy",
			"feedAmount": 5,
			"childGrowthDelay": -24000,
			"breedDelay": 6000
		},
		"TraitData": {
			"hasTraits": true
		}
	}
	```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTA3MTk3MTk1NCwyMDc1MDE3NDAzLC04ND
Q3MzA1NiwxODIyNDU2Mjg2XX0=
-->
