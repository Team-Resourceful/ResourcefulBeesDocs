## **Nether Quartz Bee**
***
This is the default Lapis Bee configuration provided by the mod. Any discrepancies should be considered as pack developer changes. This mod provides eighteen bee configurations out of the box as samples of how the customization system works. Feel free to use them as-is or change them as you wish!

```json
{  
  "flower": "ALL",  
  "maxTimeInHive": 600,  
  "hasHoneycomb": true,  
  "baseLayerTexture": "ores/lapis/lapis_bee",  
  "ColorData": {  
  "isBeeColored": false,  
  "honeycombColor": "#345ec3",  
  "modelType": "ORE"  
  },  
  "MutationData": {  
  "hasMutation": true,  
  "mutationInput": "minecraft:stone",  
  "mutationOutput": "minecraft:lapis_ore",  
  "mutationType": "BLOCK_TO_BLOCK"  
  },  
  "CentrifugeData": {  
  "hasCentrifugeOutput": true,  
  "mainOutput": "minecraft:lapis_lazuli",  
  "mainOutputCount": 8  
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
eyJoaXN0b3J5IjpbMTk0NjE4MTU1M119
-->