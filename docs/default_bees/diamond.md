## **Diamond Bee**
***
This is the default Diamond Bee configuration provided by the mod. Any discrepancies should be considered as pack developer changes. This mod provides twenty bee configurations out of the box as samples of how the customization system works. Feel free to use them as-is or change them as you wish!

```json
{  
  "flower": "ALL",  
  "maxTimeInHive": 600,  
  "hasHoneycomb": true,  
  "baseLayerTexture": "ores/diamond/diamond_bee",  
  "ColorData": {  
  "isBeeColored": false,  
  "honeycombColor": "#00ffff",  
  "modelType": "ORE"  
  },  
  "MutationData": {  
  "hasMutation": true,  
  "mutationInput": "minecraft:lava",  
  "mutationOutput": "minecraft:water",  
  "mutationType": "FLUID_TO_FLUID"  
  },  
  "CentrifugeData": {  
  "hasCentrifugeOutput": true,  
  "mainOutput": "minecraft:diamond",  
  "mainOutputCount": 1  
  },  
  "SpawnData": {  
  "canSpawnInWorld": true,  
  "biomeWhitelist": "tag:OVERWORLD",  
  "biomeBlacklist": "tag:ocean"  
  },  
  "BreedData": {  
  "isBreedable": true,  
  "parent1": "Coal",  
  "parent2": "Skeleton",  
  "feedItem": "tag:forge:ores"  
  },  
  "TraitData": {}  
}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTM1NDU4NTI3NF19
-->