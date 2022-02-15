## **Emerald Bee**
***
This is the default Emerald Bee configuration provided by the mod. Any discrepancies should be considered as pack developer changes. This mod provides twenty bee configurations out of the box as samples of how the customization system works. Feel free to use them as-is or change them as you wish!

```json
{  
  "flower": "ALL",  
  "hasHoneycomb": true,  
  "baseLayerTexture": "ores/emerald/emerald_bee",  
  "ColorData": {  
	  "isBeeColored": false,  
	  "honeycombColor": "#18eb09",  
	  "modelType": "ORE"  
  },  
  "MutationData": {  
	  "hasMutation": true,  
	  "mutationInput": "minecraft:stone",  
	  "mutationOutput": "minecraft:lava",  
	  "mutationType": "BLOCK_TO_FLUID"  
  },  
  "CentrifugeData": {  
	  "hasCentrifugeOutput": true,  
	  "mainOutput": "minecraft:emerald"  
  },  
  "SpawnData": {  
	  "canSpawnInWorld": true,  
	  "biomeWhitelist": "TAG:Mountain,Hills"  
  },  
  "BreedData": {  
	  "isBreedable": true,  
	  "spawnWeight": 4  
  },  
  "TraitData": {}  
}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMzg4MzQzNjk3XX0=
-->