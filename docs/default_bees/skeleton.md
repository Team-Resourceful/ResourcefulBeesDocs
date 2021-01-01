##  **Skeleton Bee**  

***  

This is the default Skeleton Bee configuration provided by the mod. Any discrepancies should be considered as pack developer changes. This mod provides eighteen bee configurations out of the box as samples of how the customization system works. Feel free to use them as-is or change them as you wish!  
  

```json  
{  
  "flower": "small",  
  "maxTimeInHive": 600,  
  "hasHoneycomb": true,  
  "baseLayerTexture": "skeleton/skeleton_bee",  
  "ColorData": {  
	  "isBeeColored": false,  
	  "honeycombColor": "#F6F2E6"  
  },  
  "MutationData": {  
	  "hasMutation": true,  
	  "mutationInput": "minecraft:stone",  
	  "mutationOutput": "minecraft:gravel",  
	  "mutationType": "BLOCK_TO_BLOCK"  
  },  
  "CentrifugeData": {  
	  "hasCentrifugeOutput": true,  
	  "mainOutput": "minecraft:bone"  
  },  
  "SpawnData": {  
	  "canSpawnInWorld": true,  
	  "biomeWhitelist": "tag:OVERWORLD",  
	  "biomeBlacklist": "tag:ocean",  
	  "lightLevel": "NIGHT"  
  },  
  "BreedData": {  
	  "isBreedable": true,  
	  "feedItem": "small",  
	  "feedAmount": 8  
  },  
  "TraitData": {}  
}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbNTYzNzYxMjAxXX0=
-->