***

This page contains a template for the honey jsons with ALL configurable options. This should help pack devs with making their own honey since elements only need to be modified or deleted as necessary.
!!!template "Template"
	```json
	{
		"name" : "rainbow",
		"hunger": 3,
		"honeyColor": "#FFFFFF",
		"saturation": 2,
		"isRainbow" : true,
		"honeyBlockRecipe" : true,
		"generateHoneyBlock" : true,
		"generateHoneyBlock" : true,
		"effects": [
		  {
			"effectID": "minecraft:glowing",
			"duration": 2400,
			"strength": 0,
			"chance": 1
		  },
		  {
			"effectID": "speed",
			"duration": 600,
			"strength": 2,
			"chance": 0.5
		  },
		  {
			"effectID": "ars_nouveau:mana_regen",
			"duration": 600,
			"strength": 1,
			"chance": 0.25
		  }
		]
	}
	```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE4MDI1NTYxMThdfQ==
-->
