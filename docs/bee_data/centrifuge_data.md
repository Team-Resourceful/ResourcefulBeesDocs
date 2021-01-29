# **CentrifugeData**

## **Outputs**
***

### **Has Centrifuge Output?** (Required)

`hasCentrifugeOutput` is a `true`/`false` value that when set to `true` allows a recipe to be generated for the honeycomb and honeycomb block. This value is **only** required *if* you want the bee's honeycomb to have centrifuge recipes generated, otherwise the entirety of the `centrifugeData` object can be left out of the bees json.

<br>
<br>

### **Main Centrifuge Output** (Optionally Required)

`mainOutput` is a string value in the form of `namespace:ID` that specifies the primary output of the bees honeycomb when it is put into the centrifuge. This value is required when `hasCentrifugeOutput` is set to true. This value can be  _anything_  you want to give to the player so long as it is an item in game. This includes any item from another mod. This output can also have an optional weighting value provided that determines the chance of getting the item.

Here are some examples:

`"mainOutput": "minecraft:blaze_rod"`  <---- This would make the centrifuge provide blaze rods  
`"mainOutput": "theoneprobe:probe"`  <---- This would make the centrifuge provide probes from The One Probe  
`"mainOutput": "minecraft:nether_star"`  <---- This would make the centrifuge provide nether stars  
`"mainOutput": "minecraft:barrier"`  <---- This would make the centrifuge provide barrier blocks  

<br>
<br>

### **Fluid Outputs** (Optional)

Set `hasFluidOutput` to `true` when you want the main centrifuge output to be a fluid instead of an item.

This example will output 2100mb of lava per honeycomb centrifuge process:<br>
```json
"CentrifugeData": {  
  "hasCentrifugeOutput": true,  
  "mainOutput": "minecraft:lava",  
  "mainOutputCount": 2100,  
  "hasFluidOutput": true  
},
```

<br>
<br>

### **Secondary Centrifuge Output** (Optional)

The secondary output is an optional value for the bee. You can have a "waste" item or any other item for the secondary output. This value follows the same rules as shown for the main output. If no value is supplied then the default value of "Beeswax" is provided instead. This value can also have a custom defined weighting.

Here is an example of it's usage:

`"secondaryOutput" : "minecraft:redstone_lamp"`

<br>
<br>

### **Bottle Centrifuge Output** (Optional)

The bottle output is an optional value for the bee. This output is intended to allow bees to provide a different bottled ingredient such as "Dragons Breath", however, like the other two outputs this value can be set to anything. This value defaults to "Honey Bottle" if not used. This value can also have a custom defined weighting.

_Note: Regardless of the output, if a player chooses not to supply the centrifuge with bottles, then 250mb of honey will be added to an internal honey tank._

Here is an example of it's usage:

`"bottleOutput" : "minecraft:dragon_breath"`

<br>
<br>

## **Output Weighting**
***

There are three different weight values that can be set for the centrifuge outputs. These correspond with the three different centrifuge outputs available. There is the `mainOutputWeight`, the `secondaryOutputWeight`, and the `bottleOutputWeight`. These values are *optional* and can be used to determine the chance an item has to be output from the centrifuge recipe. They are two-digit decimal numbers between 0.00 -> 1.00.

Here is an example:

```json
"CentrifugeData": {
	"hasCentrifugeOutput": true,
	"mainOutput": "minecraft:diamond",
	"mainOutputWeight": 0.40,
	"secondaryOutput": "minecraft:nether_star",
	"secondaryOutputWeight": 0.02,
	"bottleOutput": "minecraft:experience_bottle",
	"bottleOutputWeight": 0.70
}
```
<br>

In the example above, the bee's honeycomb when used in the centrifuge will have a 40% chance to output a diamond, a 2% chance to output a nether star as the secondary output, and a 70% chance to output bottles of enchanting. <br>

*Note:* The default value for Main Output is 1.0. The default value for Secondary output is 0.20. The default value for Bottle Output is 0.25.

<br>
<br>

## **Input and Output Counts**
***

### **Input** (Optional)

`mainInputCount` is a value used to determine the number of honeycombs required to process the centrifuge recipe.

### **Outputs** (Optional)

Similar to weights, there are three different output count values that can be set for the centrifuge outputs. These correspond with the three different centrifuge outputs available. There is `mainOutputCount`, `secondaryOutputCount`, and `bottleOutputCount`. These values are *optional* and can be used to determine the amount of the associated output item that is received when the recipe is processed.

Here is the previous example updated with input and output counts added:

```json
"CentrifugeData": {
	"hasCentrifugeOutput": true,
	"mainInputCount": 4,
	"mainOutput": "minecraft:diamond",
	"mainOutputWeight": 0.40,
	"mainOutputCount": 2,
	"secondaryOutput": "minecraft:nether_star",
	"secondaryOutputWeight": 0.02,
	"secondaryOutputCount": 1,
	"bottleOutput": "minecraft:experience_bottle",
	"bottleOutputWeight": 0.70,
	"bottleOutputCount": 3
}
```
<br>

In the example above, the centrifuge recipe will have a 40% chance to output **two** diamonds, a 2% chance to output **one** nether star as the secondary output, and a 70% chance to output **three** bottles of enchanting while consuming **four** honeycombs per operation. <br>

*Note:* The default for all four values is `1`

## **NBT data**

You can now add item nbt data to all of the item outputs in centrifuge recipes

There are three separate parameters to edit the nbt data for each of the outputs each pertaining to one of the ouput slots.  

`mainNBTData: {}`  
`secondaryNBTData: {}`  
`bottleNBTData: {}`  

Examples:  
```Json
"mainNBTData": {
  "display":{
    "Name": "{\"text\":\"A Stone\"}"
  }
},
"secondaryNBTData": {
  "display":{
    "Name": "{\"text\":\"Crystal Diamond\"}"
  }
},
"bottleNBTData" : {
  "Potion": "resourcefulbees:calming"
},
```
<br>
<br>

## **Template**
***

Here is a blank template showing all configurable fields in the Breed Data object:

```json
"CentrifugeData": {
	"hasCentrifugeOutput": true,
	"mainInputCount": 1,
	"mainOutput": "",
	"mainOutputWeight": 1.00,
	"mainOutputCount": 1,
  "mainNBTData": {},
	"secondaryOutput": "resourcefulbees:wax",
	"secondaryOutputWeight": 0.20,
	"secondaryOutputCount": 1,
  "secondaryNBTData": {},
	"bottleOutput": "minecraft:honey_bottle",
	"bottleOutputWeight": 0.25,
	"bottleOutputCount": 1,
  "bottleNBTData": {},
	"recipeTime": 200,
	"hasFluidoutput": false
}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEyNDk4MTgyMjUsLTE5NTAzOTA2LC0xMj
AzODY4Nzg5LC0xMDMwNzQ0NDddfQ==
-->
