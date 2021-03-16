## **Template**
***

This page contains a template for the trait jsons with ALL configurable options. This should help pack devs with making their own traits since elements only need to be modified or deleted as necessary.
!!!template "Template"
  ```json
  {
    "potionDamageEffects": [
      {
        "effectID": "minecraft:wither",
        "strength": 6
      },
      {
        "effectID": "minecraft:wither",
        "strength": 6
      }
    ],
    "damageImmunities": [
      "inFire",
      "lightningBolt",
      "onFire",
      "lava",
      "hotFloor",
      "inWall",
      "cramming",
      "drown",
      "starve",
      "cactus",
      "fall",
      "flyIntoWall",
      "generic",
      "magic",
      "wither",
      "anvil",
      "fallingBlock",
      "dragonBreath",
      "dryout"
    ],
    "potionImmunities": [
      "minecraft:poison",
      "minecraft:wither"
    ],
    "damageTypes": [
      {
        "damageTypeName": "setOnFire",
        "amplifier": 6
      },
      {
        "damageTypeNName": "explosive",
        "amplifier": 3
      }
    ],
    "specialAbilities": [
      "teleport",
      "flammable",
      "slimy"
    ],
    "particleName": "minecraft:end_rod"
  }
  ```
