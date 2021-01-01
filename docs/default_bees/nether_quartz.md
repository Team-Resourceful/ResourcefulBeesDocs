## **Nether Quartz Bee**
***
This is the default Nether Quartz Bee configuration provided by the mod. Any discrepancies should be considered as pack developer changes. This mod provides eighteen bee configurations out of the box as samples of how the customization system works. Feel free to use them as-is or change them as you wish!

```json
{  
  "flower": "minecraft:nether_wart",  
  "maxTimeInHive": 1000,  
  "hasHoneycomb": true,  
  "traits": ["nether"],  
  "ColorData": {  
	  "isBeeColored": true,  
	  "honeycombColor": "#D4CABA",  
	  "primaryColor": "#D4CABA",  
	  "secondaryColor": "#303030"  
  },  
  "MutationData": {  
	  "hasMutation": true,  
	  "mutationInput": "minecraft:netherrack",  
	  "mutationOutput": "minecraft:nether_quartz_ore",  
	  "mutationType": "BLOCK_TO_BLOCK"  
  },  
  "CentrifugeData": {  
	  "hasCentrifugeOutput": true,  
	  "mainOutput": "minecraft:quartz",  
	  "mainOutputCount": 2  
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
eyJoaXN0b3J5IjpbLTEyMTc0ODE3NTBdfQ==
-->