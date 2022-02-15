## **Ender Bee**
***
This is the default Emerald Bee configuration provided by the mod. Any discrepancies should be considered as pack developer changes. This mod provides twenty bee configurations out of the box as samples of how the customization system works. Feel free to use them as-is or change them as you wish!

```json
{  
  "flower": "minecraft:chorus_flower",  
  "hasHoneycomb": true,  
  "traits": ["ender"],  
  "maxTimeInHive": 1800,  
  "ColorData": {  
	  "isBeeColored": true,  
	  "honeycombColor": "#339786",  
	  "primaryColor": "#339786",  
	  "secondaryColor": "#303030"  
  },  
  "MutationData": {  
	  "hasMutation": true,  
	  "mutationInput": "minecraft:obsidian",  
	  "mutationOutput": "minecraft:end_stone",  
	  "mutationType": "BLOCK_TO_BLOCK"  
  },  
  "CentrifugeData": {  
	  "hasCentrifugeOutput": true,  
	  "mainOutput": "minecraft:ender_pearl",  
	  "bottleOutput" : "minecraft:dragon_breath"  
  },  
  "SpawnData": {  
	  "canSpawnInWorld": true,  
	  "biomeWhitelist": "TAG:end",  
	  "lightLevel": "NIGHT",  
	  "spawnWeight": 20  
  },  
  "BreedData": {  
	  "isBreedable": true  
  },  
  "TraitData": {  
	  "hasTraits": true  
  }  
}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbNDAwNTYzOTA4XX0=
-->