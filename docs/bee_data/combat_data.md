# **Combat Data**

## **Passive Aggressive**
***

### **isPassive** (Optional)

By default bees will get attack players when they get angry. Setting `isPassive` to true prevents the attack and anger goals from being registered to the bee. This means that the bee won't get angry or attack players at all. If you want the bee to attack the player but not deal any damage then see the next value below.

<br>
<br>

### **attackDamage** (Optional)

When a bee attacks the player, by default it deals 1 damage to the player and then inflicts poison damage over a period of time. The amount of poison damage isn't configurable, however the amount of damage on sting is configurable by using `attackDamage`. This can be any float value zero or greater.

**Note:** Zero damage is useful for when you want a bee to have positive trait effects given to the player instead of damaging the player such as the Oreo Bee.

<br>
<br>

### **removeStingerOnAttack** (Optional)

Use `removeStingerOnAttack` when you want only a specific bee to either die or not die after stinging the player. The global config value `beeDiesFromSting` by default is set to `true` and overrides this value. Set `beeDiesFromSting` to `false` if you would like to modify individual bees.

<br>
<br>

### **inflictsPoison** (Optional)

Use `inflictsPoison` when you want a specific bee to **only** deal attack damage. The global config value `beesInflictPoison` by default is set to `true` and overrides this value. Set `beesInflictPoison` to `false` if you would like to modify individual bees.

## **Template**
***
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTgwNDI3MjY4LDE5NDI3NDgxMiw2NjM2Mj
c1ODgsMTc4NTU5MTU3MV19
-->