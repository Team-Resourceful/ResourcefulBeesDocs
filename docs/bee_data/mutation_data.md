# **Mutation Data**

## **Enabling Mutations**
***

### **hasMutation** (Required)

Block Mutation is an *optional* feature for bees. It is the modded version of vanilla pollination effects. Rather than a bee potentially applying a growth tick to a flower it flies over, a bee can instead "mutate" a block into another block. To give a bee a mutation `hasMutation` must be set to `true` **and** `mutationType` must be set. Mutation Types are covered below.

<br>
<br>

## **Mutation Types**
***

`mutationType` is a REQUIRED field when giving a bee a mutation.

!!! mutation-type "NONE"
	This is used when a bee has no mutation. 
	!!! example
		`#!json "mutationType": "NONE"`


!!! mutation-type "FLUID_TO_FLUID"
	This is used when a bee mutates a fluid block into another fluid block. 
	!!! example
		`#!json "mutationType": "FLUID_TO_FLUID"`


!!! mutation-type "BLOCK_TO_FLUID"
	This is used when a bee mutates a normal block into a fluid block. 
	!!! example
		`#!json "mutationType": "BLOCK_TO_FLUID"`


!!! mutation-type "FLUID_TO_BLOCK"
	This is used when a bee mutates a fluid block into a normal block. 
	!!! example
		`#!json "mutationType": "FLUID_TO_BLOCK"`


!!! mutation-type "BLOCK_TO_BLOCK"
	This is used when a bee mutates a normal block into another normal block. 
	!!! example
		`#!json "mutationType": "BLOCK_TO_BLOCK"`


!!! mutation-type "BLOCK_TO_ITEM"
	This is used when a bee mutates a normal block into a dropped item. 
	!!! example
		`#!json "mutationType": "BLOCK_TO_ITEM"`


!!! mutation-type "ENTITY_TO_ENTITY"
	This is used when a bee mutates an entity into another entity. 
	!!! example
		`#!json "mutationType": "ENTITY_TO_ENTITY"`

## **Mutation Inputs and Outputs**
***

The `mutationInput` represents the block or blocks to be mutated and the `mutationOutput` represents the final form. For example, a bee could mutate simple stone blocks into coal ore blocks or cobblestone into lava. The `mutationInput` has the option of accepting tags, however the `mutationOutput` does not.

!!! note 
	Entity to Entity mutation is also supported by using the `entity:` prefix. Entity tags are **not** supported.

!!! note 
	In a future update we will support multiple weighted outputs. This page will be updated when they are implemented.

!!! example 
	In this example the bee will mutate a stone block into a coal ore block.
	```json
	"MutationData": {
		"hasMutation": true,
		"mutationType": "BLOCK_TO_BLOCK",
		"mutationInput": "minecraft:stone",
		"mutationOutput": "minecraft:coal_ore"
	}
	```
<br>

!!! example 
	In this example the bee will mutate any block tagged as stone into a coal ore block.
	```json
	"MutationData": {
		"hasMutation": true,
		"mutationType": "BLOCK_TO_BLOCK",
		"mutationInput": "tag:forge:stone",
		"mutationOutput": "minecraft:coal_ore"
	}
	```
<br>
!!! example 
	In this example, the bee will mutate lava into obsidian.
	```json
	"MutationData": {
		"hasMutation": true,
		"mutationType": "FLUID_TO_BLOCK",
		"mutationInput": "minecraft:lava",
		"mutationOutput": "minecraft:obsidian"
	}
	```
<br>
!!! example 
	In this example, the bee will mutate cobblestone into lava.
	```json
	"MutationData": {
		"hasMutation": true,
		"mutationType": "BLOCK_TO_FLUID",
		"mutationInput": "minecraft:cobblestone",
		"mutationOutput": "minecraft:lava"
	}
	```
<br>
!!! example 
	In this example, the bee will mutate cow into a bat.
	```json
	"MutationData": {
		"hasMutation": true,
		"mutationType": "ENTITY_TO_ENTITY",
		"mutationInput": "entity:minecraft:cow",
		"mutationOutput": "entity:minecraft:bat"
	}
	```
<br>

!!! note
	Mutation Input and Mutation Output are not limited to just Minecraft blocks. Any block from any mod can be used as long as it has a resource location in the form of `namespace:ID`. In addition, when using fluids, only fluids that have a block variant can be used.

<br>
<br>

### **mutationCount**

Use `mutationCount` when you want to specify how many blocks a bee can mutate before it must visit a hive and collect nectar again. By default a bee will mutate **ten** blocks before the process must be reset.

!!! example 
	```json
	"MutationData": {
		"hasMutation": true,
		"mutationType": "BLOCK_TO_BLOCK",
		"mutationInput": "minecraft:stone",
		"mutationOutput": "minecraft:coal_ore",
		"mutationCount": 5
	}
	```

<br>
<br>

## **Multi Mutate** (Optional)

A completely new way to register mutations, this system allows you to register as many mutations for a single bee as you want.

### **type**

This is where you put the type of mutation you want to add.

!!! example "Examples" 
	`#!json "type": "BLOCK_TO_BLOCK"`  
	`#!json "type": "BLOCK_TO_ITEM"`  
	`#!json "type": "ENTITY_TO_ENTITY"`  

### **inputID**

This is the id of the thing you want to mutate from

!!! note
	if you want to mutate a tag, you need to prefix with `tag:`, if you want to mutate an entity you need to prefix with `entity:`

!!! example "Examples" 
	`#!json "inputID": "minecraft:stone"`  
	`#!json "inputID": "tag:forge:stone"`  
	`#!json "inputID": "entity:minecraft:pig"`  

### **defaultWeight** (optional)

This will set the default weight that you will get an output if you do not specify a weight in the outputs.

!!! example "Examples"  
	`#!json "defaultWeight": 10`  
	`#!json "defaultWeight": 2`  

Default : `1`

### **chance** (optional)

This will set the default weight that you will succeed in a mutation if you do not specify a chance in the outputs.

!!! example "Examples" 
	`#!json "cdefaultChance": 1`  
	`#!json "cdefaultChance": 0.5`  

Default : `1`

### **outputs**

This is where you specify the outputs for your mutations, you can have as many different outputs as you want.

**outputID**  
this is where you specify the output id of your mutation.  

!!! note
	If your output is an entity, you need to prefix it with `entity:`  

**chance** (optional)  
This is where you set the individual success chance for your mutation outputs

Default: `1`

**weight** (optional)  
This is where you set the individual weight for your mutation outputs

Default: `1`

**nbtData** (optional)  
NBT data, yes NBT data, this is where you can now set the nbt data for your mutation outputs

**Effects**  
- Entity tags for `ENTITY_TO_ENTITY` Mutations  
- Item tags for `BLOCK_TO_ITEM` Mutations  
- Tile entity tags for `BLOCK_TO_BLOCK` and `FLUID_TO_BLOCK` Mutations  

!!! example "Examples" 
	```json
	"outputs":[
		{"outputID": "minecraft:stone", "weight": 10},
		{"outputID": "minecraft:diamond", "weight": 1}
	]
	```
	```json
	"outputs":[
		{
			"outputID": "entity:minecraft:mooshroom",
			"nbtData": {
				"Type": "brown"
			}
		},
		{
			"outputID": "entity:minecraft:mooshroom"
		}
	]
	```

### **Mutations**

You can use the new multi mutate by adding the new `mutations` parameter.

!!! example "Examples" 

	```json
	"MutationData": {
	  "hasMutation": true,
	  "mutationType": "BLOCK_TO_BLOCK",
	  "mutationInput": "minecraft:stone",
	  "mutationOutput": "minecraft:coal_ore",
	  "mutationCount": 5,
	  "mutations": [
		{
		  "type": "BLOCK_TO_BLOCK",
		  "inputID": "tag:forge:stone",
		  "chance": 0.5,
		  "outputs": [
			{"outputID": "minecraft:redstone_ore", "weight": 1}
			{"outputID": "minecraft:lapis_ore", "weight": 3}
		  ]
		},
		{
		  "type": "BLOCK_TO_BLOCK",
		  "inputID": "minecraft:honey_block",
		  "chance": 0.5,
		  "outputs": [
			{"outputID": "minecraft:glass"}
		  ]
		},
		{
		  "type": "BLOCK_TO_ITEM",
		  "inputID": "tag:forge:ores/diamond",
		  "outputs": [
			{
			  "outputID": "minecraft:potion",
			  "nbtData": {
				"Potion": "resourcefulbees:calming"
			  }
			}
		  ]
		},
		{
		  "type": "ENTITY_TO_ENTITY",
		  "inputID": "entity:cow",
		  "outputs": [
			{
			  "outputID": "entity:mooshroom",
			  "nbtData": {
				"Type": "brown"
			  }
			}
		  ]
		}
	  ]
	}
	```
<br>
<br>

***

!!! template "Template"

	Here is a blank template showing all configurable fields in the Mutation Data object:

	```json
	"MutationData": {
		"hasMutation": false,
		"mutationType": "NONE",
		"mutationInput": "",
		"mutationOutput": "",
		"mutationCount": 10,
		"mutations": [
			{
				"type": "NONE",
				"outputID": "",
				"cdefaultChance": 1,
				"defaultWeight": 1,
				"outputs": [
					{"outputID": "", "chance": 1, "weight": 1, "nbtData":{}}
				]
			}
		]
	}
	```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEyNzgxMzEyODksLTE1NjI4NDg4NDMsLT
E0OTQwODA5NzgsNzEwMTM5NjEwLDcxMjE4NDU0Miw3MzA5OTgx
MTZdfQ==
-->