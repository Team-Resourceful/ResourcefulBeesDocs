# **ColorData**

## **Color**
***

### **isBeeColored** (Required)

This value is used to determine if a bee should have its primary and secondary color layer textures colorized. This value defaults to `false` and as such it must be set to true if you wish to have colored bees. Leave the value as `false` when you want to use a custom base layer texture only. The 

<br>
<br>

### **Honeycomb Color** (Optionally Required)

The color value for the honeycomb is only a required value when the bee has the `hasHoneycomb` value set to true in the main data. 

This value can be expressed in multiple ways but is encoded in the .json as a string. It can be expressed as a hexadecimal value with, or without, preceding tags, an integer value, or a named color from the available list found [here.](https://github.com/Resourceful-Bees/ResourcefulBees/wiki/Optional-Colors-Names) The color value is used to determine the bee's honeycomb color and honeycomb block color.

Below are some examples of color usage.

`"honeycombColor": "#ff00ff"` <br>
`"honeycombColor": "#fff"` <br>
`"honeycombColor": "ff00ff"` <br>
`"honeycombColor": "0xff00ff"` <br>
`"honeycombColor": "white"` <br>

<br>
<br>

### **Primary Color & Secondary Color** (Optionally Required)

The primary and secondary color values are required only when you want the bee to be colored using the boolean value `isBeeColored`. 

These values can be expressed in multiple ways but are encoded in the .json as strings. They can be expressed as a hexadecimal value with, or without, preceding tags, an integer value, or a named color from the available list found [here.](https://github.com/Resourceful-Bees/ResourcefulBees/wiki/Optional-Colors-Names) The color values are used to colorize the primary layer and secondary layer textures for the bee. 

Below are some examples of color usage.

`"primaryColor": "#ff00ff"` <br>
`"primaryColor": "#fff"` <br>
`"primaryColor": "ff00ff"` <br>
`"secondaryColor": "0xff00ff"` <br>
`"secondaryColor": "white"` <br>

*Note:* The secondary color is not required if you would like a single color bee with black stripes. 

*Note:* The primary and secondary color are also used for coloring the bee in the bee jar and the spawn egg so supplying the primary and secondary colors with values will make those look better.

<br>
<br>

## Textures
***

### **Primary & Secondary layer textures** (Optional)

Should you wish to provide your own bee layer textures, there are two layer textures that can be customized. These textures are `primaryLayerTexture`, and `secondaryLayerTexture`. The textures can only be .png file types.

If you want to just use a texture that wont be recolored by our system you're looking for the baseLayerTexture in the main data.

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

## Special
***

### **Glow Color & Enchanted glow**

The color value for the glowing is only a required value when the bee has the `isGlowing` value set to true. 

This value can be expressed in multiple ways but is encoded in the .json as a string. It can be expressed as a hexadecimal value with, or without, preceding tags, an integer value, or a named color from the available list found [here.](https://github.com/Resourceful-Bees/ResourcefulBees/wiki/Optional-Colors-Names) The color value is used to determine the bee's honeycomb color and honeycomb block color.

Below are some examples of color usage.

`"glowColor": "#ff00ff"` <br>
`"glowColor": "#fff"` <br>
`"glowColor": "ff00ff"` <br>
`"glowColor": "0xff00ff"` <br>
`"glowColor": "white"` <br>

`isEnchanted` set to true sets the bee to have the enchantment glint effect.

**Note:** `isGlowing` and `isEnchanted` are incompatible.

<br>
<br>
<!--stackedit_data:
eyJoaXN0b3J5IjpbODA1MzEyNTc0XX0=
-->