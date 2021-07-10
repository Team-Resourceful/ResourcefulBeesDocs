Listed below are all possible options for Bee Data and what is required.

## **Name** (Required)

A bee's **type** and **name** are used interchangeably. This information is determined based on the name of the .json file containing the bee's data. This value is automatically obtained and required.

!!! note
    Bee names **must** be entered in the snake_case format.

<br>
<br>

## **Honeycomb Color** (Optionally Required)

The color value for the honeycomb is only a required value when the bee has a centrifuge output. This value can be expressed in multiple ways but is encoded in the .json as a string. It can be expressed as a hexadecimal value with, or without, preceding tags, an integer value, or a named color from the available list found [here.](https://wiki.resourcefulbees.com/en/1.15/bee_data/color_names/) The color value is used to determine the bee's honeycomb color and honeycomb block color.

!!! example "Examples"
	`#!json "honeycombColor": "#ff00ff"` <br>
	`#!json "honeycombColor": "#fff"` <br>
	`#!json "honeycombColor": "0xff00ff"` <br>
	`#!json "honeycombColor": "white"` <br>

<br>
<br>

## **Primary Color && Secondary Color** (Optionally Required)

The primary and secondary color values are required only when you want the bee to be colored using the boolean value `isBeeColored`. These values can be expressed in multiple ways but are encoded in the .json as strings. They can be expressed as a hexadecimal value with, or without, preceding tags, an integer value, or a named color from the available list found [here.](https://wiki.resourcefulbees.com/en/1.15/bee_data/color_names/) The color values are used to colorize the primary layer and secondary layer textures for the bee. 

!!! example "Examples"
  `#!json "primaryColor": "#ff00ff"` <br>
  `#!json "primaryColor": "#fff"` <br>
  `#!json "primaryColor": "ff00ff"` <br>
  `#!json "secondaryColor": "0xff00ff"` <br>
  `#!json "secondaryColor": "white"` <br>
  
!!! note
	The secondary color is not required if you would like a single color bee with black stripes.
  
<br>
<br>

## **isBeeColored** (Optional)

This value is used to determine if a bee should have its primary and secondary color layer textures colorized. This value defaults to `true`. This value should be set to `false` when you want to use a custom base layer texture only.

<br>
<br>

## **Custom Textures** (Optional)

Should you wish to provide your own bee textures, there are three different textures that can be customized. These textures are `baseLayerTexture`, `primaryLayerTexture`, and `secondaryLayerTexture`. The textures can only be .png file types.

The base layer texture is the texture used when you don't wish to have the bee colored. It also provides the eyes for the bee. When supplying your own custom texture, the texture file must be located in the `config\resourcefulbees\resources\assets\resourcefulbees\textures\entity` directory found in the mod pack's directory. In addition, *two textures* for each texture variant **must** be present: a normal texture and an angry texture. The angry texture file name must end with "_angry"

For example:<br>
![Resourceful Bees Custom Texture Filename Example](https://i.imgur.com/2sypgCS.png)
<br>

The primary and secondary layer textures are the textures used for coloring the bee. If you would like to use different gray-scaled textures then the custom texture files must be located in the `config\resourcefulbees\resources\assets\resourcefulbees\textures\entity` directory found in the mod pack's directory.

*Note:* Sub-directories are supported as you will see in the example .json below

```json
"primaryLayerTexture": "custom/alternative_primary_layer",
"secondaryLayerTexture": "custom/alternative_secondary_layer"
```
<br>

Sub-directories can be nested like so: `"folder_1/folder_2/folder_3/texture"`

**SPECIAL NOTE:** The file extension is *NOT REQUIRED* in the .json value as that is automatically appended by the mod when rendering. 

<br>
<br>

## **Flower** (Required)

The flower value is used to determine what flower the bee should use for pollen/nectar gathering. We provide a few different options for the flower value and may provide more in the future. Currently, the options available for a flower include three separate tags or a block ID as seen below. In addition, we added general block tag support as well as seen below.

`"flower": "all"`    <-------- This lets the bee use all available flowers including modded flowers.<br>
`"flower": "tall"`   <-------- This lets the bee use only flowers with the tag "tall" such as the rose bush.<br>
`"flower": "small"`  <------- This lets the bee use only flowers with the tag "small" such as the poppy.<br>

`"flower: "tag:minecraft:bee_growables"` <--- This lets the bee use any block in the crops tag and sweet berry bushes (note: bees take damage from the sweet berry bush like a player would)<br>

`"flower": "minecraft:poppy"`<br>

This final example lets the bee use only a predefined flower, including modded flowers. This value is not locked only to flowers, however. *ANY* block in the game including modded can be used here. *Note:* Flowers are not a comma-separated list. You get to choose either **ONE** flower, all flowers, tall flowers, or small flowers, in addition to Block Tags.

<br>
<br>

## **Main Centrifuge Output** (Optionally Required)

The main output value is what determines the primary output when running the bee's honeycomb through the centrifuge. This value can be *anything* you want to give to the player so long as it is an item in game. This includes any item from another mod. This output can also have an optional weighting value provided that determines the chance of getting the item.

Here are some examples:

`"mainOutput": "minecraft:blaze_rod"`  <---- This would make the centrifuge provide blaze rods <br>
`"mainOutput": "theoneprobe:probe"`    <---- This would make the centrifuge provide probes from The One Probe <br>
`"mainOutput": "minecraft:nether_star"`  <---- This would make the centrifuge provide nether stars <br>
`"mainOutput": "minecraft:barrier"`  <---- This would make the centrifuge provide barrier blocks <br>

*Note:* As of 1.15.2-0.2.4a not using this value skips honeycomb and centrifuge recipe generation for the bee. This can be useful for when you want a bee that only mutates blocks.

<br>
<br>

## **Secondary Centrifuge Output** (Optional)

The secondary output is an optional value for the bee. You can have a "waste" item or any other item for the secondary output. This value follows the same rules as shown for the main output. If no value is supplied then the default value of "Beeswax" is provided instead. This value can also have a custom defined weighting.

Here is an example of it's usage:

`"secondaryOutput" : "minecraft:redstone_lamp"`

<br>
<br>

## **Bottle Centrifuge Output** (Optional)

The bottle output is an optional value for the bee. This output is intended to allow bees to provide a different bottled ingredient such as "Dragons Breath", however, like the other two outputs this value can be set to anything. This value defaults to "Honey Bottle" if not used. This value can also have a custom defined weighting.

Here is an example of it's usage:

`"bottleOutput" : "minecraft:dragon_breath"`

<br>
<br>

## **Spawn in World** (Optionally Required)

This value is *optionally required.* This value must be either `true` or `false` depending on if you want the bee to spawn in the world or not. If the value is true then you **must** include the spawnable biomes in the biome whitelist field as will be seen in the next section.

<br>
<br>

## **Biome Whitelist && Biome Blacklist** (Optionally Required)

These values are *optionally required.* The values are comma-separated and used in combination with the "spawn in world" value. This value can be expressed in a variety of ways and as such the values are used to determine the dimension a bee may spawn in as well. It is much easier to show examples of their usage.

*Note:* You can use either [biome type tags](https://wiki.resourcefulbees.com/en/1.15/bee_data/biome_tags) or specific biomes, you cannot use both simultaneously.

This example will let the bee spawn in any nether biome.<br>
```json
"spawnInWorld": true,
"biomeWhitelist": "tag:nether"
```
<br>

This example will let the bee spawn in any overworld biome except ocean biomes.<br>
```json
"spawnInWorld": true,
"biomeWhitelist": "tag:overworld"
"biomeBlacklist": "tag:ocean"
```
<br>

This example will let the bee spawn in any mountain or hills biome except the desert hills biome.<br>
```json
"spawnInWorld": true,
"biomeWhitelist": "TAG:Mountain, HILLS"
"biomeBlacklist": "minecraft:desert_hills"
```
<br>

This example will let the bee spawn in plains, frozen river, or beach biomes only.<br>
```json
"spawnInWorld": true,
"biomeList": "minecraft:plains,minecraft:frozen_river,minecraft:beach"
```
<br>

*Note:* Take notice that letter casing and spaces have no impact on the bee's ability to spawn. However, when using a biome type tag, the prefix "tag:" **must** be included. <br>

*SPECIAL NOTE:* As of 1.15.2-0.2.4a, nests will generate in the biomes where bees are set to spawn. During generation a nest may randomly spawn additional bees consisting only of the bees allowed to spawn in the biome where the nest generated.

<br>
<br>

## **Max Time in Hive** (Optional)

This value is *optional.* This value is used to determine the amount of time **in ticks** the bee must spend in the hive before it generates a honeycomb. This value is represented as an integer value. The minimum value allowed is 600 ticks with no maximum. This value defaults to 2400 ticks, like the vanilla bee, if not set. <br>

`"maxTimeInHive": 1000` <------ This means the bee will have to stay in the hive for 1000 ticks before generating a honeycomb. <br>

<br>
<br>


## **Parent 1 & Parent 2 & Breedable** (Optionally Required)

Parent 1 and Parent 2 are two separate values. They are *optional*, however, when used, they **must** be used together with "breedable". Parent 1 and Parent 2 are used for determining what bees must mate to create this child bee. The "breedable" value is a true/false flag to tell the mod that "this bee is breedable and here are it's parents".

Here is an example of its usage:

In this example the bee can be bred when a "Diamond" and "Emerald" bee mate.<br>
```json
"breedable": true,
"parent1": "diamond",
"parent2": "Emerald"
```
<br>

In this example the bee can be bred when "my_super_cool_bee" mates with "my_other_super_cool_bee".<br>
```json
"breedable": true,
"parent1": "my_super_cool_bee",
"parent2": "my_other_super_cool_bee"
```
<br>

*Note:* A bee must have two **different** parents. No two bees can have the **same** two parents.

<br>
<br>

## **Breed Weight** (Optional)

This value is an *optional* value. This value is used when establishing a bee's breeding rules. This value is represented as a "double". The value should be between 0.00 -> 1.00. This value determines the weighting that the child bee has when breeding. The default for this value is 0.33.

Using the above here are additional breeding examples:

This example the bee has a 50% chance to spawn when a Gold and Lapis bee mate.<br>
```json
"breedable": true,
"parent1": "Gold",
"parent2": "Lapis",
"breedWeight": 0.5
```
<br>

This example the bee has a 15% chance to spawn when a Wither and Blaze bee mate.
```json
"breedable": true,
"parent1": "Wither",
"parent2": "Blaze",
"breedWeight": 0.15
```

<br>
<br>

## **Centrifuge Output Weighting** (Optional)

There are three different weight values that can be set for the centrifuge outputs. These correspond with the three different centrifuge outputs available. There is the `mainOutputWeight`, the `secondaryOutputWeight`, and the `bottleOutputWeight`. These values are *optional* and can be used to determine the chance an item has to be output from the centrifuge recipe. Like the breed weight above they are two-digit decimal numbers between 0.00 -> 1.00.

Here is an example:

```json
"mainOutput": "minecraft:diamond",
"mainOutputWeight": 0.40,
"secondaryOutput": "minecraft:nether_star",
"secondaryOutputWeight": 0.02,
"bottleOutput": "minecraft:experience_bottle",
"bottleOutputWeight": 0.70
```
<br>

In the example above, the bee's honeycomb when used in the centrifuge will have a 40% chance to output a diamond, a 2% chance to output a nether star as the secondary output, and a 70% chance to output bottles of enchanting. <br>

*Note:* The default value for Main Output is 1.0. The default value for Secondary output is 0.20. The default value for Bottle Output is 0.25.

<br>
<br>

## **Block Mutation** (Optional)

Block Mutation is an *optional* feature for bees. It is the modded version of vanilla pollination effects. Rather than a bee potentially applying a growth tick to a flower it flies over, a bee can instead "mutate" a block into another block. The `mutationInput` represents the block or blocks to be mutated and the `mutationOutput` represents the final form. For example, a bee could mutate simple stone blocks into coal ore blocks or cobblestone into lava. The `mutationInput` has the option of accepting tags, however the `mutationBlock` does not.

Example:

In this example the bee will mutate a stone block into a coal ore block.<br>
```json
"baseBlock": "minecraft:stone",
"mutationBlock": "minecraft:coal_ore"
```
<br>

In this example the bee will mutate any block tagged as stone into a coal ore block.<br>
```json
"baseBlock": "tag:forge:stone",
"mutationBlock": "minecraft:coal_ore"
```
<br>

In this example the bee will mutate a coal block into a bedrock block.<br>
```json
"baseBlock": "minecraft:coal_block",
"mutationBlock": "minecraft:bedrock"
```
<br>

In this example, the bee will mutate any fluid in the lava tag into obsidian.<br>
```json
"mutationInput": "tag:minecraft:lava",
"mutationOutput": "minecraft:obsidian"
```
<br>

In this example, the bee will mutate cobblestone into lava.<br>
```json
"mutationInput": "minecraft:cobblestone",
"mutationOutput": "minecraft:lava"
```
<br>

*Note:* Mutation Input and Mutation Output are not limited to just Minecraft blocks. Any block from any mod can be used as long as it has a resource location in the form of "namespace:id". In addition, when using fluids, only fluids that have a block variant can be used. <br>

<br>
<br>

## **Size Modifier** (Optional)

The size modifier is an optional floating point value that scales the size of the bee. This value ranges from 0.5 to 2.0. Any value entered outside this range will be automatically clamped to the range bounds. This means a value of 0.2 would become 0.5. The default value is 1.0. 

`"sizeModifier": 2.0`  <---- This would make the bee twice the size of a default bee <br>
`"sizeModifier": 0.5`  <---- This would make the bee half the size of a default bee <br>
`"sizeModifier": 1.375`  <---- This would make the bee 1 3/8 times the size of a default bee <br>

*SPECIAL NOTE:* When a bees size is modified, the child version of that bee also has it's size modified. Check out the coal bee as an example. <br>

<br>
<br>

# **Bee Traits** (Optional)

There are various *optional* traits available for bees and potentially more to come. Traits affect bees in a variety of ways such as what type of damage it does when it attacks. Below is the list of available bee traits and what they do as well as their .json syntax. *Note:* Bee traits are stackable.

## **Ender Bee**

Syntax: `"enderBee": true`   Effect: Bee will have enderman particle effects and periodically teleport up to 4 blocks from its current location.

## **Nether Bee**

Syntax: `"netherBee": true`   Effect: Bee does not take damage from fire.

## **Creeper Bee**

Syntax: `"creeperBee": true`   Effect: Bee will have a random sized explosion when attacking a player.

## **Skeleton Bee**

Syntax: `"skeletonBee": true`    Effect: Does nothing at this time.

## **ZomBee**

Syntax: `"zomBee": true`    Effect: Bee causes hunger when attacking the player.

## **Pigman Bee**

Syntax: `"pigmanBee": true`    Effect: Bee causes mining fatigue when attacking the player.

## **Wither Bee**

Syntax: `"witherBee": true`    Effect: Bee causes wither when attacking the player. Wither bee is not affected by wither.

## **Blaze Bee**

Syntax: `"blazeBee": true`    Effect: Bee will set player on fire when attacking. Bee also randomly sets itself on fire. And bee does not take damage from fire.
