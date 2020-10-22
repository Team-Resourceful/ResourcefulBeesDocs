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
"breedable": true,
"parent1": "diamond",
"parent2": "Emerald"
```
  

In this example the bee can be bred when "my_super_cool_bee" mates with "my_other_super_cool_bee".  
```json
"breedable": true,
"parent1": "my_super_cool_bee",
"parent2": "my_other_super_cool_bee"
```

_Note:_  A bee must have two  **different**  parents. No two bees can have the  **same**  two parents.
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTk4NzkyNDAwNCwtMTExMzk3ODgxMCwxMD
c4MDUwNTIsLTc1MzkxNzMwMSw4MTAwMTc3MTldfQ==
-->