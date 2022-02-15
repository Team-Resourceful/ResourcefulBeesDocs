# **Custom Traits**

***
Custom honey are made similar to how you would make a custom bee, below is information on what values you can use to customise your honey.  

When created the trait will be available for use and be automatically be added to be Beepedia  

## **beepediaItemID** (Optional)  

This is the item id for an item, this item will be used to represent the trait within the Beepedia.  

!!! example "Examples"
	`#!json "beepediaItemID": "minecraft:end_rod"`  
	`#!json "beepediaItemID": "resourcefulbees:wax"`  

	Default `#!json "minecraft:blaze_powder"`  

## **potionDamageEffects** (Optional)

This is a list of potion effects that a bee can deal when it attacks an entity.

Each list entry has to variables both of which are required.  

### **<strike>effectRegistryName</strike>** or **effectID**  

This is the effect id of the potion effect you wish to apply.  

!!! example "Examples"
	`#!json "effectID": "minecraft:poison"`  
	`#!json "effectRegistryName": "resourcefulbees:calming"`  

### **<strike>amplifier</strike>** or **strength**  

This is the strength of the potion effect you wish to apply.

!!! example "Examples"
	`#!json "strength": 2`  
	`#!json "amplifier": 0`  


!!! example "Example"
	```Json
		"potionDamageEffects": [
			{
			  "effectID": "minecraft:wither",
			  "strength": 6
			},
			{
			  "effectRegistryName": "resourcefulbees:calming",
			  "amplifier": 6
			}
  		]
  	```  

## **damageImmunities** (Optional)  

This is a list of damage immunities that will be applied to the bee  

!!! example "Valid damageTypes"
  	`#!json "inFire"`  
	`#!json "lightningBolt"`  
  	`#!json "onFire"`  
  	`#!json "lava"`  
  	`#!json "hotFloor"`  
  	`#!json "inWall"`  
  	`#!json "cramming"`  
  	`#!json "drown"`  
  	`#!json "starve"`  
  	`#!json "cactus"`  
  	`#!json "fall"`  
  	`#!json "flyIntoWall"`  
  	`#!json "generic"`  
  	`#!json "magic"`  
  	`#!json "wither"`  
  	`#!json "anvil"`  
  	`#!json "fallingBlock"`  
  	`#!json "dragonBreath"`  
  	`#!json "dryout"`  

!!! example "Example"
	```Json
	"damageImmunities" : [
		"anvil",
		"cramming"
	]
	```

## **potionImmunities** (Optional)

This is a list of potion effect immunities that will be applied to the bee  

This list is represented as a list of potion IDs  

!!! example "Example"
	```Json
		"potionImmunities": [
			"minecraft:poison",
			"resourcefulbees:calming"
		]
	```  

## **damageTypes** (Optional)

This is a list of damageTypes that a bee will inflict on dealing damage to an entity.  

see: [damageImmunities](https://wiki.resourcefulbees.com/en/1.16.3/extra_stuff/custom_traits/#damageimmunities-optional) for a list of valid damageTypes.  

Each list entry has to variables both of which are required.  

### **damageTypeName**

This is the damageType id used to determine the damage the bee will do.  

!!! example "Examples"
  	`#!json "damageTypeName": "lightningBolt"`  
  	`#!json "damageTypeName": "anvil"`  

### **amplifier**

This is the amplifier that will be applied to the damage type, not every damage type has a need for an amplifier but it is still required for the list item.  

Below are some examples of an amplifier:  

!!! example "Examples"
	  `#!json "amplifier": 2`  
	  `#!json "amplifier": 0`  


!!! example "Example"
	```Json
	"damageTypes": [
		{
			"damageTypeName": "setOnFire",
			"amplifier": 6
		},
		{
			"damageTypeNName": "explosive",
			"amplifier": 3
		}
	]
	```

## **particleName**
This is the id of a particle that a bee will emit from itself every 2 seconds.  

!!! example "Example"
	  `#!json "particleName": "minecraft:end_rod"`  

***
!!! template "Template"

  	Here is a blank template showing all configurable fields in a custom trait:

	```Json
	{
		{
			"potionDamageEffects": [
				{
					"effectID": "",
					"strength": 0
				}
			],
			"damageImmunities": [],
			"potionImmunities": [],
			"damageTypes": [
				{
					"damageTypeName": "",
					"amplifier": 0
				}
			],
			"specialAbilities": [],
			"particleName": ""
		}
	}
	```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTc0NTIwMjY1MV19
-->
