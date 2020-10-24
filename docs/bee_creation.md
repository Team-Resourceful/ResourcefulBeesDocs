With the base mod alone you get 14 bees but you can add as many bees as you want so that's what I'm going to teach you how to do.


First you'll need to locate our config folder by going to your main config folder and then going into the folder called `resourcefulbees`. Then in our config folder you'll see 2 sub folders `bees` and `resources` you'll need to then go into the `bees` if you have run the game once you'll see 14 json files named according to each added bee in-game. After you're in the `bees` folder you'll need to make a new json file with the name of the bee you want, so for example `Blaze.json` for if you want to add a blaze bee. After you've created the json file with the name of the bee you want to add, you'll need to open it. After you open it, we're going to start to write the bee's file and include all the necessary lines that are required for the bee to get registered. Here's how a json file for a blaze bee would look like:
```json
{
  "primaryColor": "#e6c153",
  "honeycombColor": "#e6c153",
  "flower": "minecraft:nether_wart",
  "baseBlock": "minecraft:netherrack",
  "mutationBlock": "minecraft:magma_block",
  "mainOutput": "minecraft:blaze_rod",
  "spawnInWorld": true,
  "biomeList": "tag:NETHER",
  "maxTimeInHive": 600,
  "blazeBee": true
}
```
Here are some other examples:

**Bee only made from 2 parents**
```json
{
  "primaryColor": "#fc8403",
  "honeycombColor": "#fc8403",
  "flower": "ALL",
  "mainOutput": "minecraft:shulker_shell",
  "breedable":true,
  "parent1":"Ender",
  "parent2":"Coal"
}
```
**Bee with different centrifuge outputs & weightings**
```json
{
  "primaryColor": "#ff0088",
  "honeycombColor": "#ff0088",
  "flower": "ALL",
  "mainOutput": "minecraft:end_crystal",
  "mainOutputWeight": 0.5,
  "secondaryOutput": "minecraft:nether_star",
  "secondaryOutputWeight": 1.0,
  "bottleOutput": "minecraft:dragon_breath",
  "bottleOutputWeight": 0.35,
  "spawnInWorld": true,
  "biomeList": "tag:OVERWORLD"
}
```
**Bee with specific biome it can spawn in**
```json
{
  "primaryColor": "#6b553d",
  "honeycombColor": "#6b553d",
  "flower": "ALL",
  "mainOutput": "minecraft:torch",
  "spawnInWorld": true,
  "biomeList": "minecraft:sunflower_plains"
}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTU1MjcyNjczMF19
-->