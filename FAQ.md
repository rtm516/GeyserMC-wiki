## How Does it Work?
Geyser works as a translator, translating both the incoming and outgoing packets to a format both the client and server can understand. With this being said, it emulates a Minecraft: Java Edition client, so the server actually thinks you're joining from Java Edition. Regardless of the server or what plugins it has installed, you can join it with Geyser (as long as the server supports the latest Minecraft version).

## What plugins don't work with Geyser?
* [ProtocolSupport](https://www.spigotmc.org/resources/protocolsupport.7201/) (Please use [ViaVersion](https://www.spigotmc.org/resources/viaversion.19254/) if you want to support other Java edition versions)

## How do I add players to the whitelist when using Floodgate?
There are two ways you can do this. The first way is to turn off the whitelist using `/whitelist off`, then get the Geyser player to join, then run `/whitelist add "username"`, then turn the whitelist back on using `/whitelist on`. The second way is to add the player's UUID as given by Floodgate to the whitelist.json file and then run `/whitelist reload`.

## How do I find a player's UUID without them joining when using Floodgate?
First, you'll need to get the XUID of the player. There's several third party websites to find this, for example [this one](https://cxkes.me/xbox/xuid) (unaffiliated with Geyser). You'll need to enter the player's Xbox gamertag, and once submitted it should display the XUID in the format of `xxxxxxxxxxxxxxxx`. In order to turn the XUID into a UUID that Java Edition can recognize, you just need to put the XUID in this format: `00000000-0000-0000-xxxx-xxxxxxxxxxxx`. If formatted right, Java Edition should accept it as a UUID.