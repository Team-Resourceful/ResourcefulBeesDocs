#Here are some examples of different bees you can make:


!!! example "Bee only made from 2 parents"

        ```Json
            {
              "primaryColor": "#fc8403",
              "honeycombColor": "#fc8403",
              "flower": "ALL",
              "mainOutput": "minecraft:shulker_shell",
              "breedable":true,
              "parent1":"Ender",
              "parent2":"Coal"
            }
        ```
  
!!! example "Bee with different centrifuge outputs & weightings"

        ```Json
            {
              "primaryColor": "#ff0088",
              "honeycombColor": "#ff0088",
              "flower": "ALL",
              "mainOutput": "minecraft:end_crystal",
              "mainOutputWeight": 0.5,
              "secondaryOutput": "minecraft:nether_star",
              "secondaryOutputWeight": 1.0,
              "bottleOutput": "minecraft:dragon_breath",
              "bottleOutputWeight": 0.35,
              "spawnInWorld": true,
              "biomeList": "tag:OVERWORLD"
            }
        ```
  
!!! example "Bee with specific biome it can spawn in"

        ```Json
            {
              "primaryColor": "#6b553d",
              "honeycombColor": "#6b553d",
              "flower": "ALL",
              "mainOutput": "minecraft:torch",
              "spawnInWorld": true,
              "biomeList": "minecraft:sunflower_plains"
            }
        ```
