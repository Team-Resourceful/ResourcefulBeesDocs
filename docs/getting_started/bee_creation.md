## **Creating a Bee**
***

With the base mod alone you get 14 bees but you can add as many bees as you want and modify the existing bees.

* First locate the `resourcefulbees` config folder inside the main config folder.
* Inside this folder you'll see a sub folder labeled `bees`.
* If you have run the game at least once, you'll see 14 .json files named according to each bee added by the mod inside the `bees` folder. 
* Create a .json file inside this folder for each bee you wish to add to the game. So for example: `Blaze.json` if you want to add a blaze bee.
* After you've created the json file with the name of the bee you want to add, you'll need to open it. After you open it, we're going to start to write the bee's file and include all the necessary lines that are required for the bee to get registered. You can find all Bee Data that can be put into the json here. 
* Here's how a json file for a blaze bee would look like:
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
* For every custom bee, entries will need to be add to a [language file](https://resourceful-bees.readthedocs.io/en/1.16.3/getting_started/language_files/) so the names of the bee and associated items/blocks display correctly in-game. 

* [Visit our discord if you need any further assistance](https://discord.gg/resourcefulbees)
