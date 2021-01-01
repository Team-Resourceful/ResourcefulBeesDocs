## **Coal Bee**
***
This is the default Coal Bee configuration provided by the mod. Any discrepancies should be considered as pack developer changes. This mod provides twenty bee configurations out of the box as samples of how the customization system works. Feel free to use them as-is or change them as you wish!

```json
{  
  "flower": "ALL",  
  "maxTimeInHive": 600,  
  "hasHoneycomb": true,  
  "baseLayerTexture": "ores/coal/coal_bee",  
  "ColorData": {  
	  "isBeeColored": false,  
	  "honeycombColor": "#303030",  
	  "modelType": "ORE"  
  },  
  "MutationData": {  
	  "hasMutation": true,  
	  "mutationInput": "tag:forge:stone",  
	  "mutationOutput": "minecraft:coal_ore",  
	  "mutationType": "BLOCK_TO_BLOCK"  
  },  
  "CentrifugeData": {  
	  "hasCentrifugeOutput": true,  
	  "mainOutput": "minecraft:coal",  
	  "mainOutputCount": 16  
  },  
  "SpawnData": {  
	  "canSpawnInWorld": true,  
	  "biomeWhitelist": "tag:overworld",  
	  "biomeBlacklist": "tag:ocean"  
  },  
  "BreedData": {  
	  "feedItem": "minecraft:poppy",  
	  "feedAmount": 4,  
	  "isBreedable": true  
  },  
  "TraitData": {}  
}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTUwODI2OTkwMF19
-->