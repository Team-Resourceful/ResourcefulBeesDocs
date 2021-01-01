## **Creeper Bee (Beeper)**
***
This is the default Creeper Bee configuration provided by the mod. Any discrepancies should be considered as pack developer changes. This mod provides twenty bee configurations out of the box as samples of how the customization system works. Feel free to use them as-is or change them as you wish!

```json
{  
  "flower": "ALL",  
  "maxTimeInHive": 600,  
  "hasHoneycomb": true,  
  "baseLayerTexture": "/creeper/creeper_bee",  
  "traits" : ["creeper"],  
  "ColorData": {  
	  "isBeeColored": false,  
	  "honeycombColor": "#0C9F0A",  
	  "isGlowing": true,  
	  "glowColor": "#E2D3D3",  
	  "glowingPulse": 2,  
	  "emissiveLayerTexture": "/creeper/creeper_bee_emissive"  
  },  
  "MutationData": {  
	  "hasMutation": true,  
	  "mutationInput": "tag:minecraft:lava",  
	  "mutationOutput": "minecraft:mossy_cobblestone",  
	  "mutationType": "FLUID_TO_BLOCK"  
  },  
  "CentrifugeData": {  
	  "hasCentrifugeOutput": true,  
	  "mainOutput": "minecraft:gunpowder",  
	  "mainOutputCount": 4  
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
eyJoaXN0b3J5IjpbODIwMjY0MjgwXX0=
-->