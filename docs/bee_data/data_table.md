|Data|Prerequisite|Type|Default Value|Additional Information|
|:----------:|:---------:|:---------:|:-----------:|--------------|
|flower|none|String|none|Flower used for pollination|
|isBeeColored|none|Boolean|true|Enables bee coloring system|
|primaryColor|isBeeColored|String|none|Primary bee color|
|secondaryColor|isBeeColored|String|none|Secondary bee color (stripes)|
|honeycombColor|isBeeColored|String|none|Color of the honey comb produced by the bee|
|mainOutput|none|String|none|Main output of the centrifuge when processign this bee's honeycomb|
|secondaryOutput|none|String|resourcefulbees:beeswax|Secondary output of the centrifuge when processign this bee's honeycomb|
|bottleOutput|none|String|minecraft:honey_bottle|Does not have to strictly output a honey bottle|
|mainInputCount|none|int|1|Quantity of combs needed for recipe|
|mainOutputWeight|mainOutput|double|1.0|Percent chance to recive the main output item|
|secondaryOutputWeight|secondaryOutput|double|0.2|Percent chance to recive the secondary output item|
|bottleOutputWeight|bottleOutput|double|0.25|Percent chance to recive the honey bottle (or specified alternate) item|
|mainOutputCount|mainOutput|int|1|Quantity of the main output item. Can be greater than 64|
|secoundaryOutputCount|secondaryOutput|int|1|Quantity of the secondary output item. Can be greater than 64|
|bottleOutputCount|bottleOutput|int|1|Quantity of the honey bottle (or specified alternate) output item. Can be greater than 64|
|breedable|none|boolean|none|Is this bee breedable?|
|parent1|breedable|String|none|What bee type is this bee's first parent?|
|parent2|breedable|String|none|What bee type is this bee's second parent?|
|breedWeight|breedable|double|0.33|What is the likelihood of receiving this bee when breeding. Value can be any positive number. Note: values under 1.0 are multiplied by 100|
|feedItem|none|String|all|Item required to breed bee. Can use tags|
|feedAmount|none|int|1|Quantity of feed item needed to trigger "love" state|
|spawnInWorld|none|boolean|none|Can this bee naturally spawn in the world?|
|biomeWhitelist|spawnInWorld|String|none|What biomes can this bee spawn in? (Comma separated list. Can use tags)|
|biomeBlacklist|spawnInWorld|String|none|What biomes can this bee **NOT** spawn in? (Comma separated list. Can use tags)|
|spawnWeight|spawnInWorld|int|10|What is the likelihood of this bee spawning in the whitelisted biomes vs other bees whitelisted to the same biomes? Can be any positive number greater than 0|
|mutationInput|none|String|none|What block will this bee mutate? Can use Tags|
|mutationOutput|mutationInput|String|none|What will the input block mutate into?|
|mutationCount|mutationInput|int|10|How many blocks can this bee mutate per trip to its hive?|
|isGlowing|none|boolean|false|Can this bee glow? Note: Emissive light only. Does not provide actual world lighting|
|glowingColor|isGlowing|String|#ffffff|What color will this bee glow?|
|isEnchanted|none|boolean|false|Gives the bee an enchantment appearance|
|baseLayerTexture|none|String|/custom/bee|Can supply a custom texture for the bee. Note: Must include a "_bee.png" and "_bee_angry.png" version|
|primaryLayerTexture|none|String|/custom/primary_layer|Can supply a custom primary color layer texture when coloring bees|
|secondaryLayerTexture|none|String|/custom/secondary_layer|Can supply a custom secondary color layer texture when coloring bees|
|maxTimeInHive|none|int|2400|Max time in ticks the bee will stay in a T1 hive before producing a honeycomb. Min value is 600 with no max|
|attackDamage|none|float|1.0|How much damage will this bee do the player when attacking? Note: Does not affect specialty bee traits|
|sizeModifier|none|float|1.0|Scales the bee model bigger or smaller. Range is 0.5 -> 2.0|

|Traits|Effects|
|:-:|-|
|enderBee|Bee randomly teleports up to 4 blocks along its path|
|netherBee|Bee doesn't take fire damage|
|creeperBee|Bee explodes when attacking player with a random sized explosion|
|skeletonBee|Not currently used|
|zomBee|Causes hunger when attacking player|
|pigmanBee|Causes mining fatigue when attacking player|
|witherBee|Causes wither when attacking player|
|blazeBee|Deals fire damage when attacking player|
|canSwim|Prevents bee from drowning|
