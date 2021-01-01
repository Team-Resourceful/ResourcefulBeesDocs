##  **Zombee**  

***  

This is the default Zombee configuration provided by the mod. Any discrepancies should be considered as pack developer changes. This mod provides eighteen bee configurations out of the box as samples of how the customization system works. Feel free to use them as-is or change them as you wish!  
  

```json  
{  
  "flower": "tag:minecraft:bee_growables",  
  "maxTimeInHive": 600,  
  "hasHoneycomb": true,  
  "baseLayerTexture": "zombie/zombie_bee",  
  "traits": ["zombie"],  
  "ColorData": {  
  "isBeeColored": false,  
  "honeycombColor": "#2F4E32"  
  },  
  "MutationData": {  
  "hasMutation": true,  
  "mutationInput": "minecraft:stone",  
  "mutationOutput": "minecraft:cobblestone",  
  "mutationType": "BLOCK_TO_BLOCK"  
  },  
  "CentrifugeData": {  
  "hasCentrifugeOutput": true,  
  "mainOutput": "minecraft:rotten_flesh"  
  },  
  "SpawnData": {  
  "canSpawnInWorld": true,  
  "biomeWhitelist": "tag:OVERWORLD",  
  "biomeBlacklist": "tag:ocean",  
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
eyJoaXN0b3J5IjpbMjYwNzkzMzQxXX0=
-->