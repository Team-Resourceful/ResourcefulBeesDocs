## **Language Files**
***

When creating custom bees, a language file needs to be created and entries provided so all corresponding items and blocks  have proper names otherwise they will look something like this:<br>
`item.resourcefulbees.blaze_honeycomb`<br>

_Note: For new mod installs, run the game at least once so all necessary config files and folders can be generated_
***
Locate the `resourcefulbees` config folder inside 

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
eyJoaXN0b3J5IjpbLTE1NTEwMTY2NzIsMTI5NzAwNDkyNV19
-->