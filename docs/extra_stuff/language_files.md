#

When creating custom bees, your custom bees and all corresponding items and blocks will not have proper names they will look something like this `item.resourcefulbees.blaze_honeycomb`, so I'm going to teach you how to add the needed lang files to turn the long names into simple more readable names.
***
First make sure you've loaded the mod once so that the necessary folders are created.
Then go to the config directory and find the `resourcefulbees` folder and inside of there you will see 2 folders `bees` and `resources` you will need to go into the `resources` folder and you'll see a file called `pack.mcmeta` this file is needed for the loading of the language files if you do not see this file reload the mod to generate it.
Now that you've located the resource folder you will need to make a folder inside of the resource folder called `assets` then you'll need to create another folder called `resourcefulbees` inside of that folder and then you'll need to make one final folder called `lang` inside of that folder. You'll have a folder structure looking like this: 

![](https://i.imgur.com/Sq9sp1e.png)

After you have the folder structure setup we are now going to make a file called `en_us.json` or have the file named to the language you have your game set to you can find all available language codes [here](https://minecraft.gamepedia.com/Language) under the **Available languages** section.

After you have made the language file corresponding to the language you're making the lang file for you'll need to fill the file with something like this:
```json
{
   "block.resourcefulbees.blaze_honeycomb_block": "Blaze Honeycomb Block",
   "item.resourcefulbees.blaze_honeycomb": "Blaze Honeycomb",
   "item.resourcefulbees.blaze_spawn_egg": "Blaze Bee Spawn Egg",
   "entity.resourcefulbees.blaze_bee": "Blaze Bee"
}
```
Now just restart the game and you have made your custom bees, items and blocks have proper names.

**NOTE** You do not need multiple lang files you only need one and just add new lines for each new bee you would like to add so it would look like this: 
```json
{
   "block.resourcefulbees.blaze_honeycomb_block": "Blaze Honeycomb Block",
   "item.resourcefulbees.blaze_honeycomb": "Blaze Honeycomb",
   "item.resourcefulbees.blaze_spawn_egg": "Blaze Bee Spawn Egg",
   "entity.resourcefulbees.blaze_bee": "Blaze Bee",
   "block.resourcefulbees.pig_honeycomb_block": "Pig Honeycomb Block",
   "item.resourcefulbees.pig_honeycomb": "Pig Honeycomb",
   "item.resourcefulbees.pig_spawn_egg": "Pig Bee Spawn Egg",
   "entity.resourcefulbees.pig_bee": "Pig Bee"
}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTM2ODE1MTk2N119
-->