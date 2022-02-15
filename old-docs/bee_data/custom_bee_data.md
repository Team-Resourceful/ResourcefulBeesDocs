# **Custom Bee Data**

## **Core Bee data**
***

### **Name**

A bees **type** and **name** are used interchangeably. This information is determined based on the name of the .json file containing the bee's data. This value is automatically obtained and required.

!!! note
    Bee names **must** be entered in the snake_case format.

<br>
<br>

### **Flower** (Required)

The flower value is used to determine what flower the bee should use for pollen/nectar gathering. We provide a few different options for the flower value and may provide more in the future. Currently, the options available for a flower include three separate tags or a block ID as seen below. In addition, we've added general block tag support as well.

!!! note
	Block tag support does not include fluid tags. Fluids must be specified by the source block name only.
!!! example "Examples"

	`#!json "flower": "all"`    <-------- This lets the bee use all available flowers including modded flowers.<br>
	`#!json "flower": "tall"`   <-------- This lets the bee use only flowers with the tag "tall" such as the rose bush.<br>
	`#!json "flower": "small"`  <------- This lets the bee use only flowers with the tag "small" such as the poppy.<br>

	`#!json "flower": "tag:minecraft:bee_growables"` <--- This lets the bee use any block in the crops tag and sweet berry bushes (note: bees take damage from the sweet berry bush like a player would)<br>

	`#!json "flower": "minecraft:poppy"`

	This final example lets the bee use only a predefined flower, including modded flowers. This value is not locked only to flowers, however. *ANY* block in the game including modded can be used here since it takes a string value in the form of `namespace:ID`.

!!! note
	Flowers are not a comma-separated list. You get to choose either **ONE** flower, all flowers, tall flowers, or small flowers, in addition to Block Tags.

<br>
<br>

### **Has Honeycomb?** (Required)

`hasHoneycomb` is a required value. When set to `true` the honeycomb and honeycomb block for the bee will be registered as well as the associated crafting recipes. A bee can have honeycombs registered without having centrifuge recipes generated for the comb.

<br>
<br>

### **Size Modifier** (Optional)

The size modifier is an optional floating point value that scales the size of the bee. This value ranges from 0.5 to 2.0. Any value entered outside this range will be automatically clamped to the range bounds. This means a value of 0.2 would become 0.5. The default value is 1.0.

`#!json "sizeModifier": 2.0`  <---- This would make the bee twice the size of a vanilla bee<br>
`#!json "sizeModifier": 0.5`  <---- This would make the bee half the size of a vanilla bee<br>
`#!json "sizeModifier": 1.375`  <---- This would make the bee 1 3/8 times the size of a vanilla bee<br>

!!! note
	When a bees size is modified, the child version of that bee also has its size modified. Check out the icy bee as an example.

<br>
<br>

### **Bee Traits** (Optional)

There are various *optional* traits available for bees and potentially more to come. Traits affect bees in a variety of ways such as what type of damage it does when it attacks. Traits are added to a bee by specifying them in the `traits[]` string array.
!!! note
	Bee traits are stackable.

!!! example "Examples"
	`#!json "traits" : ["creeper"]`
	`#!json "traits": ["nether", "pigman"]`

<br>
<br>

### **Max Time in Hive** (Optional)

This value is *optional.* This value is used to determine the amount of time **in ticks** the bee must spend in the hive before it generates a honeycomb. This value is represented as an integer value. The minimum value allowed is `600` ticks with no maximum. This value defaults to `2400` ticks, like the vanilla bee, if not set.

`#!json "maxTimeInHive": 1000` <------ This means the bee will have to stay in the hive for `1000` ticks before generating a honeycomb.

<br>
<br>

## **Custom Textures**
***

Should you wish to provide your own custom bee texture, there is one `baseLayerTexture` that can be customized.
!!! note
	Textures can only be .png file types.

The base layer texture is the texture used when you don't wish to have the bee colored. It also provides the eyes for the bee when using the colored variants. When supplying your own custom texture, the texture file must be located in the `config\resourcefulbees\resources\assets\resourcefulbees\textures\entity` directory found in the mod pack's directory. In addition, *two textures* for each texture variant **must** be present: a normal texture and an angry texture. The angry texture file name must end with `_angry`

For example:
![Resourceful Bees Custom Texture Filename Example](https://i.imgur.com/2sypgCS.png)

!!! note
	Sub-directories are supported as you will see in the example .json below

	```json
	"baseLayerTexture": "/creeper/creeper_bee"
	```

Sub-directories can be nested like so: `"folder_1/folder_2/folder_3/texture"`

!!! important
	The file extension is *NOT REQUIRED* in the .json value as that is automatically appended by the mod when rendering.

<br>
<br>

## **Base Model Type** (Optional)

If you want to change the base model of the bee, you can use the following value to change it, there are currently only two options `DEFAULT`, and `KITTEN`. Default is your default basic bee, and kitten makes them gain little cat ears, a little nose and some soft fluffy feet.

!!! example
	`#!json "baseModelType" : "KITTEN"`

<br>
<br>

## **Additional Data**
***

### **Custom Honeycombs** (Optional)

If you wish to have a bee output something other than a honeycomb you can do so by specifying the `custombCombDrop` and `customCombBlockDrop` fields. The Oreo bee makes use of this by outputting cookies instead of honeycombs. You **must** still set `hasHoneycomb` to true. Internally, we will know if you've supplied custom outputs and adjust accordingly.

These fields use the `namespace:ID` format.

!!! example

	```json
	"hasHoneycomb": true,
	"customCombDrop": "minecraft:iron",
	"customCombBlockDrop": "minecraft:iron_block"
	```

<br>
<br>

### **Apiary Output Amounts** (Optional)

`apiaryOutputAmounts[]` is an integer array. The array consists of **four** values each corresponding to the appropriate tier apiary. For example the Oreo bee uses this data option:

```json
"apiaryOutputAmounts" : [1,2,3,4]
```

!!! note
	You can specify any value of zero or greater. Specifying a value of `-1` defaults to the global output amounts set in the common config file.

<br>

### **Breed Data** (Optional)

This is a json object that groups all breed related options. See Breed Data for more info.

<br>

### **Centrifuge Data** (Optional)

This is a json object that groups all centrifuge related options. See Centrifuge Data for more info.

<br>

### **Color Data** (Optional)

This is a json object that groups all color related options. See Color Data for more info.

<br>

### **Combat Data** (Optional)

This is a json object that groups all combat related options. See Combat Data for more info.

<br>

### **Mutation Data** (Optional)

This is a json object that groups all mutation related options. See Mutation Data for more info.

<br>

### **Spawn Data** (Optional)

This is a json object that groups all spawn related options. See Spawn Data for more info.

<br>

### **Trait Data** (Optional)

This is a json object that groups all trait related options. See Trait Data for more info.

<br>
<br>

### **Additional Data** (Optional)

Through the use of our API other mods can make their own data options. The mods would be required to handle their own parsing of the data and syntax for the data. Soon we will be adding Java Docs to our classes to help improve the API experience. Any and all feedback is welcome for improving our API either through PR requests or github issues.

<br>

***

!!! template "Template"

	Here is a Custom Bee Data template which shows the format for the core json itself. We will have a separate template page which has a **full template** containing *ALL* configurable options.

	```json
	{
		"flower": "ALL",
		"maxTimeInHive": 2400,
		"hasHoneycomb": true,
		"sizeModifier": 1.0,
		"baseLayerTexture": "/custom/bee",  
		"traits" : [""],
		"customCombDrop": "",
		"customBombBlockDrop": "",
		"apiaryOutputAmounts" : [1,2,3,4],
		"ColorData": {  
			"isBeeColored": false
		}
		"MutationData": {  
			"hasMutation": false,
			"mutationType": "NONE"
		},
		"CentrifugeData": {  
			"hasCentrifugeOutput": false,  
		},  
		"SpawnData": {  
			"canSpawnInWorld": false
		},
		"BreedData": {  
			"isBreedable": false
		},
		"TraitData": {}
	}
	```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjEzODIxODE0MywtMTc3MDgzMTQ2LC0yMD
g4NzQ2NjEyXX0=
-->
