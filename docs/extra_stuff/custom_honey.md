# **Custom honey**
***

Custom honey are made similar to how you would make a custom bee, below is information on what values you can use to customise your honey

currently custom honey blocks, honey bottles, honey buckets, and honey fluids will all be generated from the below Data. It will also be added the Beepedia automatically.

## **ID Names**

the ids of the custom items will be generated using the file name or an optional "name" field in the file

!!! example "Examples"
	`#!json "name": "sweet"`  
	`#!json "name": "rainbow"`  

!!! note
	Here is how the IDs will be formated.

	Honey bottle: {name}_honey_bottle  
	Honey block: {name}_honey_block  
	Honey bucket: {name}_honey_fluid_bucket  
	Honey fluid: {name}_honey  

## **Food Data**

### **hunger** (optional)

This value determines how much hunger you'll get on drinking the honey

!!! example "Examples"
	`#!json "hunger": 2`  
	`#!json "hunger": 0`  

Default: 1

### **saturation** (optional)

This value determines how much saturation you'll gain on drinking the honey

!!! example "Examples"
	`#!json "saturation": 0.5`  
	`#!json "saturation": 4`  
	`#!json "saturation": 2.0`  

Default: 1.0

## **Colour Data**

### **honeyColour** (optional)

This value can be expressed in multiple ways but is encoded in the .json as a string. It can be expressed as a hexadecimal value with, or without, preceding tags, an integer value, or a named color from the available list found [here.](https://resourceful-bees.readthedocs.io/en/1.16.3/extra_stuff/color_names/) The color value is used to determine the honey's color.

Below are some examples of color usage.
!!! example "Examples"
	`#!json "honeyColour": "#ff00ff"`  
	`#!json "honeyColour": "#fff"`  
	`#!json "honeyColour": "ff00ff"`  
	`#!json "honeyColour": "0xff00ff"`  
	`#!json "honeyColour": "white"`  

Default: #ffffff

### **isRainbow** (optional)

This value determines if the color of the honey is rainbow or not

!!! example "Example"
	`#!json "isRainbow": true`  

Default: false

### **honeyBlockRecipe** (optional)

This value determines if a recipe for a honey block and back to bottles is generated.

!!! example "Example"
	`#!json "honeyBlockRecipe": false`  

Default: true

### **generateHoneyBlock** (optional)

This value determines if a honey block is generated.

!!! example "Example"
	`#!json "generateHoneyBlock": false`  

Default: true

### **generateHoneyFluid** (optional)

This value determines if honey fluid and a honey bucket are generated.

!!! example "Example"
	`#!json "generateHoneyFluid": false`  

Default: true

## **Custom Effects**

### **effects** (optional)

This value is a list of effects that will be applied when you drink the honey.
This value is an object made up of all of the below effect options, you can add as many objects as you like so long as you don't duplicate the effects used.

!!! example "Example"
	```Json
	"effects": [
		{
			"effectID": "minecraft:speed",
			"duration": 1200
		},
		{
			"effectID": "strength",
			"strength": 2,
			"chance": 0.25
		},
		{
			"effectID": "ars_nouveau:mana_regen",
			"duration": 600,
			"strength": 1,
			"chance": 0.5
		}
	]
	```

### **effectID** (required)

This value is the effect id you would use to apply a potion effect, make sure if it's a modded potion effect the mod id is used.

!!! example "Examples"
	`#!json "effectID": "speed"`  
	`#!json "effectID": "minecraft:strength"`  
	`#!json "effectID": "ars_nouveau:mana_regen"`  
	`#!json "effectID": "modname:potion_id"`  

### **duration** (optional)

This value is the time in ticks that the potion effect will be applied to you when you consume the honey.
Note: One second is 20 ticks.

!!! example "Examples"
	`#!json "duration": 600`  
	`#!json "duration": 2400`  

Default: 60

### **strength** (optional)

This value determines the strength of the potion effect given when you comsume the honey.

!!! example "Examples"
	`#!json "strength": 0`  
	`#!json "strength": 2`  

Default: 0

### **chance** (optional)

This value determines how often the potion effect is applied when you comsome the honey.
This value is a float value that represents a value out of 100, 1 being 100%, 0.5 being 50% 0.01 being 1% and so on.

!!! example "Examples"
	`#!json "chance": 0.3`  
	`#!json "chance": 1`  

Default: 1

## **Language Data**

***
When creating custom honey, all corresponding items and blocks and fluids will not have proper names they will look something like this `item.resourcefulbees.blaze_honeycomb`, similar to how custom bees work, meaning you will need to set up your lang file with all the new values added by the custom honey

Here is an example on how you should add your custom honey to your lang file.

!!! example "Example"
	```json
	{
		 "item.resourcefulbees.rainbow_honey_bottle": "Rainbow Honey Bottle",
		 "item.resourcefulbees.rainbow_honey_fluid_bucket": "Rainbow Honey Bucket",
		 "block.resourcefulbees.rainbow_honey_block": "Rainbow Honey Block",
		 "fluid.resourcefulbees.rainbow_honey": "Rainbow Honey"
	}
	```

**Note:**	Like all other default lang values, if you set generateEnglishLang = true in the client.toml in the resourcefulbees config folder default values for honey will be generated as well, keep in mind this will also auto generate all of the bee lang values as well, so use with caution.

[Get some extra information on how to set up lang files here.](https://resourceful-bees.readthedocs.io/en/1.16.3/getting_started/language_files/)

***
!!! template "Template"

	Here is a blank template showing all configurable fields in custom honey:

	```Json
	{
		"name" : "",
		"hunger": 0,
		"honeyColor": "#FFFFFF",
		"saturation": 0,
		"isRainbow" : true,
		"honeyBlockRecipe" : true,
		"generateHoneyBlock" : true,
		"generateHoneyBlock" : true,
		"effects": [
			{
				"effectID": "",
				"duration": 0,
				"strength": 0,
				"chance": 0
			}
		]
	}
	```
