With Geyser being a protocol translator between two different games with two different codebases, there are a handful of limitations that Geyser is unfortunately unable to handle. Despite Minecraft Bedrock and Java being quite close in comparison, there are some vast differences in many areas.

The following things cannot be fixed without changes to Bedrock or the Java protocol in general. As of now, they are not fixable in Geyser.

- Custom heads in inventories
- Clickable links in chat
- Glowing effect
- Crafting in the 2x2 menu while in creative mode
- Distinguishing between left and right clicks in inventories
- Redstone dot blockstates
- "Can be placed on/destroyed" tag for *some* blocks - for example, different colors of clay/wool that don't exist as separate blocks
- Potion colors implemented using NBT
- Various command arguments for any command that doesn't use the Minecraft Brigadier library
- Unable to see banner layers past 6
- Movement issues around bamboo due to offset differences between Java and Bedrock
- Custom anvil recipes
- Heights lower than 0 or above 256 on non-beta versions of Bedrock

The following changes **are supported** with the [GeyserOptionalPack](https://github.com/GeyserMC/Geyser/wiki/GeyserOptionalPack), which is a Bedrock resource pack you can install for additional functionality for features Bedrock does not natively support:
- Custom armor stand poses
- Illusioners
- Iron golem cracked texture
- Hit particles and other miscellaneous particles not natively in Bedrock
- Offhand animations
- Shulker invisibility
- Spectral arrow texture