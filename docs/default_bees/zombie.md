##  **ZombBee**  

***  

This is the default Netherite Bee configuration provided by the mod. Any discrepancies should be considered as pack developer changes. This mod provides eighteen bee configurations out of the box as samples of how the customization system works. Feel free to use them as-is or change them as you wish!  
  

```json  
{  
  "flower": "minecraft:wither_rose",  
  "maxTimeInHive": 600,  
  "hasHoneycomb": true,  
  "baseLayerTexture": "ores/netherite/netherite_bee",  
  "traits": ["nether", "wither"],  
  "ColorData": {  
  "isBeeColored": false,  
  "honeycombColor": "#654740"  
  },  
  "MutationData": {  
  "hasMutation": true,  
  "mutationInput": "minecraft:blackstone",  
  "mutationOutput": "minecraft:gilded_blackstone",  
  "mutationType": "BLOCK_TO_BLOCK"  
  },  
  "CentrifugeData": {  
  "hasCentrifugeOutput": true,  
  "mainOutput": "minecraft:netherite_ingot",  
  "mainOutputWeight": 0.05  
  },  
  "SpawnData": {  
  "canSpawnInWorld": true,  
  "biomeWhitelist": "tag:nether",  
  "lightLevel": "NIGHT"  
  },  
  "BreedData": {  
  "isBreedable": true,  
  "parent1": "Wither",  
  "parent2": "Diamond"  
  },  
  "TraitData": {  
  "hasTraits": true  
  }  
}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTYxNjEwNDQwXX0=
-->