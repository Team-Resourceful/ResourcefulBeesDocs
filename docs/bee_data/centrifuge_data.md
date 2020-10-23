# **CentrifugeData**

## **Outputs**
***

### **hasCentrifugeOutput** (Required)

This is a `true`/`false` value that when set to `true` allows a recipe to be generated for the honeycomb and honeycomb block. This value is **only** required *if* you want the bee's honeycomb to have centrifuge recipes generated, otherwise the entirety of the `centrifugeData` object can be left out of the bees json. 

<br>
<br>

### **mainOutput** (Optionally Required)

The main output value is what determines the primary output when running the bee's honeycomb through the centrifuge. This value can be  _anything_  you want to give to the player so long as it is an item in game. This includes any item from another mod. This output can also have an optional weighting value provided that determines the chance of getting the item.

Here are some examples:

`"mainOutput": "minecraft:blaze_rod"`  <---- This would make the centrifuge provide blaze rods  
`"mainOutput": "theoneprobe:probe"`  <---- This would make the centrifuge provide probes from The One Probe  
`"mainOutput": "minecraft:nether_star"`  <---- This would make the centrifuge provide nether stars  
`"mainOutput": "minecraft:barrier"`  <---- This would make the centrifuge provide barrier blocks  

_Note:_  As of 1.15.2-0.2.4a not using this value skips honeycomb and centrifuge recipe generation for the bee. This can be useful for when you want a bee that only mutates blocks.

`mainOutput` is a string value in the form of `namespace:ID` that specifies the primary output of the bees honeycomb. This value is required when `hasCentrifugeOutput` is set to true. 
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE1MDg1MDA2MjhdfQ==
-->