## **Dragon Bee**
***
This is the default Dragon Bee configuration provided by the mod. Any discrepancies should be considered as pack developer changes. This mod provides twenty bee configurations out of the box as samples of how the customization system works. Feel free to use them as-is or change them as you wish!

```json
{
  "flower": "minecraft:obsidian",
  "maxTimeInHive": 2400,
  "hasHoneycomb": true,
  "baseLayerTexture" : "dragon/dragon_bee",
  "traits": [ "ender", "nether", "wither" ],
  "ColorData": {
    "isBeeColored": true,
    "isGlowing": true,
    "modelType": "DRAGON",
    "primaryLayerTexture": "dragon/dragon_bee_primary",
    "secondaryLayerTexture": "dragon/dragon_bee_secondary",
    "emissiveLayerTexture": "dragon/dragon_bee_emissive",
    "primaryColor": "#222222",
    "secondaryColor": "#171717",
    "glowColor": "#E400FF",
    "honeycombColor": "#E400FF"
  },
  "MutationData": {
    "hasMutation": true,
    "mutations" : [
      {
        "type": "BLOCK",
        "inputID": "minecraft:stone",
        "chance": 0.5,
        "outputs": [
          {"outputID": "minecraft:end_stone", "weight": 10}
        ]
      }
    ]
  },
  "CentrifugeData": {
    "hasCentrifugeOutput": true,
    "mainOutput": "minecraft:dragon_egg",
    "bottleOutput": "minecraft:dragon_breath",
    "mainOutputWeight": 0.01,
    "bottleOutputWeight": 0.5
  },
  "SpawnData": {},
  "BreedData": {
    "isBreedable": true,
    "parent1": "Wither",
    "parent2": "Ender",
    "feedItem": "minecraft:end_stone",
    "feedAmount": 12
  },
  "TraitData": {
    "hasTraits": true
  }
}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTg5MDUyNTYxNF19
-->
