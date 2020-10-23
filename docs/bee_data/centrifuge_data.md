# **CentrifugeData**

## **Outputs**
***

### **hasCentrifugeOutput** (Required)

This is a `true`/`false` value that when set to `true` allows a recipe to be generated for the honeycomb and honeycomb block. This value is **only** required *if* you want the bee's honeycomb to have centrifuge recipes generated, otherwise the entirety of the `centrifugeData` object can be left out of the bees json. 

<br>
<br>

### **mainOutput** (Optionally Required)

`mainOutput` is a string value in the form of `namespace:ID` that specifies the primary output of the bees honeycomb when it is put into the centrifuge. This value is required when `hasCentrifugeOutput` is set to true. This value can be  _anything_  you want to give to the player so long as it is an item in game. This includes any item from another mod. This output can also have an optional weighting value provided that determines the chance of getting the item.

Here are some examples:

`"mainOutput": "minecraft:blaze_rod"`  <---- This would make the centrifuge provide blaze rods  
`"mainOutput": "theoneprobe:probe"`  <---- This would make the centrifuge provide probes from The One Probe  
`"mainOutput": "minecraft:nether_star"`  <---- This would make the centrifuge provide nether stars  
`"mainOutput": "minecraft:barrier"`  <---- This would make the centrifuge provide barrier blocks  

<!--stackedit_data:
eyJoaXN0b3J5IjpbNDY0NjAyNjMyXX0=
-->