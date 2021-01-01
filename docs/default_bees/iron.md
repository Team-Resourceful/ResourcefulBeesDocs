## **Iron Bee**
***
This is the default Iron Bee configuration provided by the mod. Any discrepancies should be considered as pack developer changes. This mod provides eighteen bee configurations out of the box as samples of how the customization system works. Feel free to use them as-is or change them as you wish!

```json
{  
  "flower": "ALL",  
  "hasHoneycomb": true,  
  "maxTimeInHive": 600,  
  "baseLayerTexture": "ores/iron/iron_bee",  
  "ColorData": {  
  "isBeeColored": false,  
  "honeycombColor": "#ffcc99",  
  "modelType": "ORE"  
  },  
  "MutationData": {  
  "hasMutation": true,  
  "mutationInput": "minecraft:stone",  
  "mutationOutput": "minecraft:iron_ore",  
  "mutationType": "BLOCK_TO_BLOCK"  
  },  
  "CentrifugeData": {  
  "hasCentrifugeOutput": true,  
  "mainOutput": "minecraft:iron_ingot"  
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
eyJoaXN0b3J5IjpbLTMyMzg0MjY1OV19
-->