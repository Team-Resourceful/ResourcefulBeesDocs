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

### **NONE**

This is used when a bee has no mutation. ex. `"mutationType": "NONE"`


### **FLUID_TO_FLUID**

This is used when a bee mutates a fluid block into another fluid block. ex. `"mutationType": "FLUID_TO_FLUID"`


### **BLOCK_TO_FLUID**

This is used when a bee mutates a normal block into a fluid block. ex. `"mutationType": "BLOCK_TO_FLUID"`


### **FLUID_TO_BLOCK**

This is used when a bee mutates a fluid block into a normal block. ex. `"mutationType": "FLUID_TO_BLOCK"`


### **BLOCK_TO_BLOCK**

This is used when a bee mutates a normal block into another normal block. ex. `"mutationType": "BLOCK_TO_BLOCK"`


### **ENTITY_TO_ENTITY**

This is used when a bee mutates an entity into another entity. ex. `"mutationType": "ENTITY_TO_ENTITY"`
**NOTE:** No other form of entity mutation is planned at this time.

## **Mutation Inputs and Outputs**
***

The `mutationInput` represents the block or blocks to be mutated and the `mutationOutput` represents the final form. For example, a bee could mutate simple stone blocks into coal ore blocks or cobblestone into lava. The `mutationInput` has the option of accepting tags, however the `mutationOutput` does not.

**NOTE** Entity to Entity mutation is also supported by using the `"entity:` prefix. Entity tags are **not** supported.

**Note 2** In a future update we will support multiple weighted outputs. This page will be updated when they are implemented.

Example:

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

_Note: Mutation Input and Mutation Output are not limited to just Minecraft blocks. Any block from any mod can be used as long as it has a resource location in the form of `namespace:ID`. In addition, when using fluids, only fluids that have a block variant can be used._

<br>
<br>

### **mutationCount**

Use `mutationCount` when you want to specify how many blocks a bee can mutate before it must visit a hive and collect nectar again. By default a bee will mutate **ten** blocks before the process must be reset.

Example:

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

## **Template**
***

Here is a blank template showing all configurable fields in the Mutation Data object:

```json
"MutationData": {
	"hasMutation": false,
	"mutationType": "NONE",
	"mutationInput": "",
	"mutationOutput": "",
	"mutationCount": 10
}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTk4ODcyMTg2Miw3MTAxMzk2MTAsNzEyMT
g0NTQyLDczMDk5ODExNl19
-->