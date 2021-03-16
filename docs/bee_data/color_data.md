# **Color Data**

## **Color**
***

### **isBeeColored** (Required)

This value is used to determine if a bee should have its primary and secondary color layer textures colorized. This value defaults to `false` and as such it must be set to `true` if you wish to have colored bees. Leave the value as `false` when you want to use a custom base layer texture only. The `Diamond` and `Creeper` default bees are good examples of this.

<br>
<br>

### **Honeycomb Color** (Optionally Required)

The color value for the honeycomb is only a required value when the bee has the `hasHoneycomb` value set to true in the main data.

This value can be expressed in multiple ways but is encoded in the .json as a string. It can be expressed as a hexadecimal value with, or without, preceding tags, an integer value, or a named color from the available list found [here.](https://github.com/Resourceful-Bees/ResourcefulBees/wiki/Optional-Colors-Names) The color value is used to determine the bee's honeycomb color and honeycomb block color.

!!! example "Examples"
	`#!json "honeycombColor": "#ff00ff"` <br>
	`#!json "honeycombColor": "#fff"` <br>
	`#!json "honeycombColor": "ff00ff"` <br>
	`#!json "honeycombColor": "0xff00ff"` <br>
	`#!json "honeycombColor": "white"` <br>

<br>
<br>

### **Primary Color & Secondary Color** (Optionally Required)

The primary and secondary color values are required only when you want the bee to be colored using the boolean value `isBeeColored`.

These values can be expressed in multiple ways but are encoded in the .json as strings. They can be expressed as a hexadecimal value with, or without, preceding tags, an integer value, or a named color from the available list found [here.](https://github.com/Resourceful-Bees/ResourcefulBees/wiki/Optional-Colors-Names) The color values are used to colorize the primary layer and secondary layer textures for the bee.

!!! example "Examples"
	`#!json "primaryColor": "#ff00ff"` <br>
	`#!json "primaryColor": "#fff"` <br>
	`#!json "primaryColor": "ff00ff"` <br>
	`#!json "secondaryColor": "0xff00ff"` <br>
	`#!json "secondaryColor": "white"` <br>

!!! note
	The secondary color is not required if you would like a single color bee with black stripes.

!!! note
	The primary and secondary color are also used for coloring the bee in the bee jar and the spawn egg so supplying the primary and secondary colors with values will make those look better.

<br>
<br>

## **Textures**
***

### **Primary & Secondary layer textures** (Optional)

Should you wish to provide your own bee layer textures, there are two layer textures that can be customized. These textures are `primaryLayerTexture`, and `secondaryLayerTexture`. The textures can only be .png file types.

If you want to just use a texture that wont be recolored by our system you're looking for the baseLayerTexture in the main data.

The primary and secondary layer textures are the textures used for coloring the bee. If you would like to use different gray-scaled textures then the custom texture files must be located in the `config\resourcefulbees\resources\assets\resourcefulbees\textures\entity` directory found in the mod pack's directory.

!!! note
	Sub-directories are supported as you will see in the example .json below

!!! example
	```json
	"primaryLayerTexture": "custom/alternative_primary_layer",
	"secondaryLayerTexture": "custom/alternative_secondary_layer"
	```

Sub-directories can be nested like so: `"folder_1/folder_2/folder_3/texture"`

!!! note
	The file extension is NOT REQUIRED in the .json value as that is automatically appended by the mod when rendering.

## **Models**
***

Currently we do not allow for full-fledged model customization, however, we do provide a few model options out of the box:<br>


### **Ore** (Optional)

The `ORE` `modelType` should be used when you want the bee to have "ore crystals" rendered on its back.

!!! example
	`#!json "modelType": "ORE"`

### **Gelatinous** (Optional)

The `GELATINOUS` `modelType` should be used when you want the bee to have a slime or honey block type appearance. This model type renders a translucent "gel layer."

!!! example
	`#!json "modelType": "GELATINOUS"`

### **Dragon** (Optional)

The `DRAGON` `modelType` should be used when you want the bee to have dragon horns and spines rendered on it's back.

!!! example
	`#!json "modelType": "DRAGON"`

### **Queen** (Optional)

The `QUEEN` `modelType` should be used when you want the bee to have a pretty crown rendered on it's head.

!!! example
	`#!json "modelType": "QUEEN"`

### **Villager** (Optional)

The `VILLAGER` `modelType` should be used when you want the bee to have a nose rendered on it's face, it looks at you disapprovingly.

!!! example
	`#!json "modelType": "VILLAGER"`

### **Mushroom** (Optional)

The `MUSHROOM` `modelType` should be used when you want the bee to have 2 mushrooms on it's back and a nice layer of mycelium or other foliage on it's back.

!!! example
	`#!json "modelType": "MUSHROOM"`

### **Crop** (Optional)

The `CROP` `modelType` should be used when you want the bee to crops growing on it's back and a nice layer of foliage on it's back.

!!! example
	`#!json "modelType": "CROP"`

### **Armored** (Optional)

The `ARMORED` `modelType` should be used if you want to armor up your bee.

!!! example
	`#!json "modelType": "ARMORED"`

<br>

## **Special**
***

### **Glow Color & Enchanted Glow** (Optional)

The color value for glowing is only a required value when the bee has the `isGlowing` value set to `true`.

This value can be expressed in multiple ways but is encoded in the .json as a string. It can be expressed as a hexadecimal value with, or without, preceding tags, an integer value, or a named color from the available list found [here.](https://wiki.resourcefulbees.com/en/1.16.3/extra_stuff/color_names/) The color value is used to determine the bee's honeycomb color and honeycomb block color.

!!! example "Examples"

	`#!json "glowColor": "#ff00ff"` <br>
	`#!json "glowColor": "#fff"` <br>
	`#!json "glowColor": "ff00ff"` <br>
	`#!json "glowColor": "0xff00ff"` <br>
	`#!json "glowColor": "white"` <br>

`isEnchanted` set to true sets the bee to have the enchantment glint effect.

!!! note
	`isGlowing` and `isEnchanted` are incompatible.

<br>

### **is Rainbow Bee** (Optional)

Set `isRainbowBee` to `true` when you want the bee to cycle through a rainbow of colors. Setting this option removes the need for a primary and secondary color.

`#!json "isRainbowBee": true`<br>

<br>
<br>

***

!!! template "Template"

	Here is the Color Data Template:

	```json
	"ColorData": {
		"primaryColor":"#005500",
		"secondaryColor":"#005500",
		"honeycombColor":"#005500",
		"primaryLayerTexture":"/custom/primary_layer",
		"secondaryLayerTexture":"/custom/secondary_layer",
		"emissiveLayerTexture":"/creeper/creeper_bee_emissive",
		"isBeeColored": true,
		"isRainbowBee": false,
		"isGlowing" : true,
		"glowColor" : "#55ff55",
		"isEnchanted" : false,
		"glowingPulse" : 2,
		"modelType": "DEFAULT"
	}
	```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTg3NjMwNTE0NCw4ODE1OTI0ODEsMzI2Nj
Q0NzYwXX0=
-->
