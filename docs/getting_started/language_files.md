## **Language Files**
***

When creating custom bees, a language file needs to be created and entries provided so all corresponding items and blocks  have proper names otherwise they will look something like this:<br>
`item.resourcefulbees.blaze_honeycomb`<br>

_Note: For new mod installs, run the game at least once so all necessary config files and folders can be generated_
***
* Locate the `resourcefulbees` config folder inside the main config folder. 
* Before we begin the process of adding a language file we need to verify that specific resource and data pack files have been generated.
* Inside the `resourcefulbees` folder there should be another  folder labeled `resources`
* Open this folder and verify there is a file inside called `pack.mcmeta` - this file is needed for the loading of the language files. If you do not see this file then reload the mod/pack to generate it.
* Inside the `resources` folder we need to add the following nested folders: `assets/resourcefulbees/lang`
* The structure should appear as the following image: 
* ![](https://i.imgur.com/Sq9sp1e.png)
* Inside the `lang` folder, creating a file called `en_us.json` will create an English US language file.
* You can specify a different language using any one of the language codes found [here](https://minecraft.gamepedia.com/Language) under the **Available languages** section.
* Every custom bee added should have language entries similar to the Blaze example below:
* ````json
{
   "block.resourcefulbees.blaze_honeycomb_block": "Blaze Honeycomb Block",
   "item.resourcefulbees.blaze_honeycomb": "Blaze Honeycomb",
   "item.resourcefulbees.blaze_spawn_egg": "Blaze Bee Spawn Egg",
   "entity.resourcefulbees.blaze_bee": "Blaze Bee"
}
````
* You can either restart the game or use F3+T to reload assets and have the language file take effect.

*Note: You do not need multiple language files. You only need one with new lines added for each custom bee:*<br> 
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

## **English Lang Generator**
***

As a convenience feature, we have provided an English Lang generator that will output a language file in the proper location with translations for every custom bee used. In the `client.toml` config file is an option to enable or disable the generator. This generator only needs to be run **once** after all custom bees have been added.

_Note: The generator uses the .json file names for generating the translations._
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTA5Njg5MjAsMTcwMDM4NTEzNiwxMTYxMj
M0MjIxLDEyOTcwMDQ5MjVdfQ==
-->