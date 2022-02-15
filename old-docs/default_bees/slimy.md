##  **Slimy Bee**  

***  

This is the default Slimy Bee configuration provided by the mod. Any discrepancies should be considered as pack developer changes. This mod provides eighteen bee configurations out of the box as samples of how the customization system works. Feel free to use them as-is or change them as you wish!  
  

```json  
{  
  "flower": "all",  
  "hasHoneycomb": false,  
  "traits": ["slimy"],  
  "maxTimeInHive": 1200,  
  "baseLayerTexture": "slime/slime_bee",  
  "ColorData": {  
	  "modelType": "GELATINOUS",  
	  "gelLayerTexture": "/slime/slime_gel_Layer"  
  },  
  "MutationData": {  
	  "hasMutation": true,  
	  "mutationInput": "minecraft:honey_block",  
	  "mutationOutput": "minecraft:slime_block",  
	  "mutationType": "BLOCK_TO_BLOCK",  
	  "mutationCount": 15  
  },  
  "BreedData": {  
	  "isBreedable": true,  
	  "parent1": "rgbee",  
	  "parent2": "zombie"  
  },  
  "TraitData": {  
	  "hasTraits": true  
  }  
}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEyODEzNjAyODJdfQ==
-->