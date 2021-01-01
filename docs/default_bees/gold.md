## **Gold Bee**
***
This is the default Gold Bee configuration provided by the mod. Any discrepancies should be considered as pack developer changes. This mod provides eighteen bee configurations out of the box as samples of how the customization system works. Feel free to use them as-is or change them as you wish!

```json
{  
  "flower": "ALL",  
  "hasHoneycomb": true,  
  "maxTimeInHive": 800,  
  "baseLayerTexture": "ores/gold/gold_bee",  
  "ColorData": {  
	  "isBeeColored": false,  
	  "honeycombColor": "#FFDC00",  
	  "modelType": "ORE"  
  },  
  "MutationData": {  
	  "hasMutation": true,  
	  "mutationInput": "minecraft:stone",  
	  "mutationOutput": "minecraft:gold_ore",  
	  "mutationType": "BLOCK_TO_BLOCK"  
  },  
  "CentrifugeData": {  
	  "hasCentrifugeOutput": true,  
	  "mainOutput": "minecraft:gold_ingot"  
  },  
  "SpawnData": {  
	  "canSpawnInWorld": true,  
	  "biomeWhitelist": "tag:OVERWORLD",  
	  "biomeBlacklist": "tag:ocean"  
  },  
  "BreedData": {  
	  "isBreedable": true  
  },  
  "TraitData": {}  
}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTUxOTQzNzY4XX0=
-->