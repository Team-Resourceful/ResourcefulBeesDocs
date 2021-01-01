##  **Pigman Bee**  

***  

This is the default Pigman Bee configuration provided by the mod. Any discrepancies should be considered as pack developer changes. This mod provides eighteen bee configurations out of the box as samples of how the customization system works. Feel free to use them as-is or change them as you wish!  
  

```json  
{  
  "flower": "minecraft:brown_mushroom",  
  "maxTimeInHive": 1000,  
  "hasHoneycomb": true,  
  "baseLayerTexture": "pigman/pigman_bee",  
  "traits": ["nether", "pigman"],  
  "ColorData": {  
	  "isBeeColored": false,  
	  "honeycombColor": "#885956"  
  },  
  "MutationData": {  
	  "hasMutation": true,  
	  "mutationInput": "minecraft:netherrack",  
	  "mutationOutput": "minecraft:glowstone",  
	  "mutationType": "BLOCK_TO_BLOCK"  
  },  
  "CentrifugeData": {  
	  "hasCentrifugeOutput": true,  
	  "mainOutput": "minecraft:glowstone_dust"  
  },  
  "SpawnData": {  
	  "canSpawnInWorld": true,  
	  "biomeWhitelist": "tag:nether",  
	  "lightLevel": "NIGHT"  
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
eyJoaXN0b3J5IjpbMTkzNDAwMDk0Nl19
-->