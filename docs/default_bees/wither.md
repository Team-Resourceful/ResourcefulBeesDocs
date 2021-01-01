##  **Wither Bee**  

***  

This is the default Wither Bee configuration provided by the mod. Any discrepancies should be considered as pack developer changes. This mod provides eighteen bee configurations out of the box as samples of how the customization system works. Feel free to use them as-is or change them as you wish!  
  

```json  
{  
  "flower": "minecraft:wither_rose",  
  "maxTimeInHive": 600,  
  "hasHoneycomb": true,  
  "baseLayerTexture": "wither/wither_bee",  
  "traits": ["nether", "wither"],  
  "ColorData": {  
	  "isBeeColored": false,  
	  "honeycombColor": "#444444"  
  },  
  "MutationData": {  
	  "hasMutation": true,  
	  "mutationInput": "minecraft:lava",  
	  "mutationOutput": "minecraft:obsidian",  
	  "mutationType": "FLUID_TO_BLOCK"  
  },  
  "CentrifugeData": {  
	  "hasCentrifugeOutput": true,  
	  "mainOutput": "minecraft:nether_star",  
	  "mainOutputWeight": 0.01  
  },  
  "SpawnData": {},  
  "BreedData": {  
	  "isBreedable": true,  
	  "parent1": "Coal",  
	  "parent2": "Skeleton",  
	  "feedItem": "minecraft:rotten_flesh",  
	  "feedAmount": 12  
  },  
  "TraitData": {  
	  "hasTraits": true  
  }  
}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE4MDcxNTk3NTldfQ==
-->