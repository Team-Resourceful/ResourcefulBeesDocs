##  **Redstone Bee**  

***  

This is the default Redstone Bee configuration provided by the mod. Any discrepancies should be considered as pack developer changes. This mod provides eighteen bee configurations out of the box as samples of how the customization system works. Feel free to use them as-is or change them as you wish!  
  

```json  
{  
  "flower": "ALL",  
  "maxTimeInHive": 800,  
  "hasHoneycomb": true,  
  "baseLayerTexture": "ores/redstone/redstone_bee",  
  "ColorData": {  
  "isBeeColored": false,  
  "honeycombColor": "#aa0f01",  
  "modelType": "ORE"  
  },  
  "MutationData": {  
  "hasMutation": true,  
  "mutationInput": "minecraft:stone",  
  "mutationOutput": "minecraft:redstone",  
  "mutationType": "BLOCK_TO_BLOCK"  
  },  
  "CentrifugeData": {  
  "hasCentrifugeOutput": true,  
  "mainOutput": "minecraft:redstone",  
  "mainOutputCount": 4  
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
eyJoaXN0b3J5IjpbMjExOTUzMDU2Nl19
-->