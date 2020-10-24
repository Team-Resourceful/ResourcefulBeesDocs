# **Custom Bee Data**

## **Core Bee data**
***

### **Name**

A bees **type** and **name** are used interchangeably. This information is determined based on the name of the .json file containing the bee's data. This value is automatically obtained and required.

*Note:* Bee names **must** be entered in the snake_case format.

<br>
<br>

### **Flower** (Required)

The flower value is used to determine what flower the bee should use for pollen/nectar gathering. We provide a few different options for the flower value and may provide more in the future. Currently, the options available for a flower include three separate tags or a block ID as seen below. In addition, we've added general block tag support as well.

*Note:* Block tag support does not include fluid tags. Fluids must be specified by the source block name only.

`"flower": "all"`    <-------- This lets the bee use all available flowers including modded flowers.<br>
`"flower": "tall"`   <-------- This lets the bee use only flowers with the tag "tall" such as the rose bush.<br>
`"flower": "small"`  <------- This lets the bee use only flowers with the tag "small" such as the poppy.<br>

`"flower: "tag:minecraft:bee_growables"` <--- This lets the bee use any block in the crops tag and sweet berry bushes (note: bees take damage from the sweet berry bush like a player would)<br>

`"flower": "minecraft:poppy"`<br>

This final example lets the bee use only a predefined flower, including modded flowers. This value is not locked only to flowers, however. *ANY* block in the game including modded can be used here since it takes a string value in the form of `namespace:ID`. 

**Note:** Flowers are not a comma-separated list. You get to choose either **ONE** flower, all flowers, tall flowers, or small flowers, in addition to Block Tags.

<br>
<br>


<!--stackedit_data:
eyJoaXN0b3J5IjpbMzQ3OTU0MTAzLC0yMDg4NzQ2NjEyXX0=
-->