# **BreedData**

## **Parents and Weight**
***

### **isBreedable** (Optional)

The `isBreedable` value is a `true`/`false` flag to tell the mod that "this bee is breedable and here are it's parents".
The value defaults to `false` and must be set to `true` if you want the bee to be breedable. Setting the value to `true` but *not* specifying the bees parents means the bee can only be bred by bees of the same type.

<br>
<br>

### **Parent 1 & Parent 2** (Optionally Required)

`parent1` and `parent2` are two separate values. They are  _optional_, however, when used, they  **must**  be used together with `isBreedable`. Parent 1 and Parent 2 are used for determining what bees must mate to create this child bee.

Here is an example of its usage:

In this example the bee can be bred when a "Diamond" and "Emerald" bee mate.  

```json
"isBreedable": true,
"parent1": "diamond",
"parent2": "Emerald"
```
  

In this example the bee can be bred when "my_super_cool_bee" mates with "my_other_super_cool_bee".  
```json
"isBreedable": true,
"parent1": "my_super_cool_bee",
"parent2": "my_other_super_cool_bee"
```

A bee can also have multiple sets of parents by comma separating the values. Here is an example:
```json
"isBreedable": true,
"parent1": "coal, redstone, lapis",
"parent2": "gold, diamond, emerald"
```
Using the example above the bee would have 3 possible sets of parents:

 1. Coal & Gold
 2. Redstone & Diamond
 3. Lapis & Emerald

<br>
<br>

### **Breed Weight** (Optional)

This value is an  _optional_  value. This value is used when establishing a bee's breeding rules. This value is represented as a `double`. The value can be any number greater than zero. This value determines the weighting that the child bee has when breeding. The default for this value is 10.

Using the above information here are additional examples:

This example the bee has a 50% chance to spawn when a Gold and Lapis bee mate.  

"breedable": true,
"parent1": "Gold",
"parent2": "Lapis",
"breedWeight": 0.5

  

This example the bee has a 15% chance to spawn when a Wither and Blaze bee mate.

"breedable": true,
"parent1": "Wither",
"parent2": "Blaze",
"breedWeight": 0.15
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTEyOTk2NDc2NywtMTk5Mjk0NTQxOCwtMT
ExMzk3ODgxMCwxMDc4MDUwNTIsLTc1MzkxNzMwMSw4MTAwMTc3
MTldfQ==
-->