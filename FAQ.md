## How Does it Work?
Geyser works as a translator, translating both the incoming and outgoing packets to a format both the client and server can understand. With this being said, it emulates a Minecraft: Java Edition client, so the server actually thinks you're joining from Java Edition. Regardless of the server or what plugins it has installed, you can join it with Geyser (as long as the server supports the latest Minecraft version).

## What plugins don't work with Geyser?
* [ProtocolSupport](https://www.spigotmc.org/resources/protocolsupport.7201/)

## How do I add players to the whitelist when using Floodgate?
There are two ways you can do this. The first way is to turn off the whitelist using `/whitelist off`, then get the Geyser player to join, then run `/whitelist add "username"`, then turn the whitelist back on using `/whitelist on`. Or you can add the player's UUID as given by Floodgate to the whitelist.json file and then run `/whitelist reload`.