---
sidebar_position: 2
id: language_files
title: Language Files
---

## **How to Create**
***

:::info
When creating custom bees, a language file needs to be created and entries provided so all corresponding items and blocks  have proper names otherwise they will look something like this:

```
item.resourcefulbees.blaze_honeycomb
```
:::

:::caution
For new mod installs, run the game at least once so all necessary config files and folders can be generated
:::

### **Verify `pack.mcmeta` Exists**
***
Before we begin the process of adding a language file we need to verify that specific resource and data pack files have been generated.
Locate the `resourcefulbees` config folder inside the main config folder and open it. 
Inside the `resourcefulbees` folder there should be another folder labeled `resources`
Open this folder and verify there is a file inside called `pack.mcmeta` - this file is needed for the loading of the language files. 
:::caution
If you do not have a `pack.mcmeta` file then reload the mod/pack to generate it.
:::


### **Add the `lang` Folder**
***
Inside the `resources` folder we need to add the following nested folders: 
```
assets/resourcefulbees/lang
```

<details>
    <summary>The structure should appear as the following image:</summary>
    <div>
    <img src="https://i.imgur.com/aJFidH0.png" alt="Lang file location image"/>
    </div>
</details>


### **Create an `en-us.json` File**
***
Inside the `lang` folder, creating a file called `en_us.json` will create an English US language file.
:::tip
You can specify a different language using any one of the language codes found [here](https://minecraft.gamepedia.com/Language) under the **Available languages** section.
:::

Every custom bee added should have language entries similar to the Blaze example below:
```json title="config/resourcefulbees/resources/assets/resourcefulbees/lang/en-us.json"
{
   "block.resourcefulbees.blaze_honeycomb_block": "Blaze Honeycomb Block",
   "item.resourcefulbees.blaze_honeycomb": "Blaze Honeycomb",
   "item.resourcefulbees.blaze_spawn_egg": "Blaze Bee Spawn Egg",
   "entity.resourcefulbees.blaze_bee": "Blaze Bee"
}
```
:::tip
You can either restart the game or use F3+T to reload assets and have the language file take effect.
:::

:::note
You do not need multiple language files. You only need one with new lines added for each custom bee:
```json title="config/resourcefulbees/resources/assets/resourcefulbees/lang/en-us.json"
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
:::

## **English Lang Generator**
***

As a convenience feature, we have provided an English Lang generator that will output a language file in the proper location with translations for every custom bee used. In the `client.toml` config file is an option to enable or disable the generator. This generator only needs to be run **once** after all custom bees have been added.

:::note
The generator uses the .json file names for generating the translations.
:::