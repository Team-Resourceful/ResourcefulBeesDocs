# Custom honey
  
Custom honey are made similar to how you would make a custom bee, below is information on what values you can use to customise your honey

## Food Data

### hunger (optional)
  
This value determines how much hunger you'll get on drinking the honey  
  
Below are some examples of hunger usage.

`"hunger": 2`  
`"hunger": 0`  
  
Default: 1
  
### saturation (optional)
  
This value determines how much saturation you'll gain on drinking the honey

Below are some examples of saturation usage.

`"saturation": 0.5`  
`"saturation": 4`  
`"saturation": 2.0`  
  
Default: 1.0

## Colour Data

### honeyColour (optional)
  
This value can be expressed in multiple ways but is encoded in the .json as a string. It can be expressed as a hexadecimal value with, or without, preceding tags, an integer value, or a named color from the available list found [here.](https://github.com/Resourceful-Bees/ResourcefulBees/wiki/Optional-Colors-Names) The color value is used to determine the honey's color.

Below are some examples of color usage.

`"honeyColour": "#ff00ff"`  
`"honeyColour": "#fff"`  
`"honeyColour": "ff00ff"`  
`"honeyColour": "0xff00ff"`  
`"honeyColour": "white"`  
  
Default: #ffffff

### isRainbow (optional)

This value determines if the color of the honey is rainbow or not
  
Example  
  
`"isRainbow": true`  
  
Default: false
  
## Custom Effects

### effects (optional)  
  
This value is a list of effects that will be applied when you drink the honey.  
This value is an object made up of all of the below effect options, you can add as many objects as you like so long as you don't duplicate the effects used.
  
Below is an example of effect usage.  
  
```Json
"effects": [
  {
    "effectID": "minecraft:speed",
    "duration": 1200
  },
  {
    "effectID": "strength",
    "strength": 2,
    "chance": 0.25
  },
  {
    "effectID": "ars_nouveau:mana_regen",
    "duration": 600,
    "strength": 1,
    "chance": 0.5
  }
]
```

### effectID (required)
  
This value is the effect id you would use to apply a potion effect, make sure if it's a modded potion effect the mod id is used.
  
Below are some examples of an effectID.
  
`"effectID": "speed"`  
`"effectID": "minecraft:strength"`  
`"effectID": `"ars_nouveau:mana_regen"`
`"effectID": "modname:potion_id"`  

### duration (optional)
  
This value is the time in ticks that the potion effect will be applied to you when you consume the honey.  
Note: One second is 20 ticks.  
  
Below are some examples of duration usage.
  
`"duration": 600`  
`"duration": 2400`
  
Default: 60  
  
### strength (optional)
  
This value determines the strength of the potion effect given when you comsume the honey.  

Below are some examples of strength usage.  
  
`"strength": 0`  
`"strength": 2`  
  
Default: 0  
  
## chance (optional)
  
This value determines how often the potion effect is applied when you comsome the honey.  
This value is a float value that represents a value out of 100, 1 being 100%, 0.5 being 50% 0.01 being 1% and so on.  

Below are some examples of chance usage.
  
`"chance": 0.3`  
`"chance": 1`  
  
Default: 1  

