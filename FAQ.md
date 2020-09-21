## How Does it Work?
Geyser works as a translator, translating both the incoming and outgoing packets to a format both the client and server can understand. With this being said, it emulates a Minecraft: Java Edition client, so the server actually thinks you're joining from Java Edition. Regardless of the server or what plugins it has installed, you can join it with Geyser (as long as the server supports the latest Minecraft version).

## So how does redstone work?

Redstone will work exactly like Java Edition, since you are joining a Java Edition server and Geyser does not modify server behavior.

## What plugins don't work with Geyser?

Geyser should generally work fine with plugins, as we emulate a Java client. There are exceptions, though:

* [TCPShield](https://tcpshield.com/) does not work at this time unless you disable `only-allow-proxy-connections`. 

Floodgate can cause issues with plugins as it modifies the login process.

* [JPremium](https://www.spigotmc.org/resources/27766/) alters the UUID of a player causing Floodgate to not be able to get the Bedrock data from its map.
* ~~[ProtocolSupport](https://www.spigotmc.org/resources/7201/) sometimes causes issues with Floodgate saying `Invalid packet id: 27`. Use [ViaVersion](https://www.spigotmc.org/resources/19254/) instead if this keeps occurring~~ ProtocolSupport now works with the latest Floodgate.
* [ProtocolSupportBungee](https://www.spigotmc.org/resources/8733/) changes how the login process works and therefore breaks the floodgate injection code.
* [SayNoToMcLeaks](https://www.spigotmc.org/resources/40906/) prevents Floodgate from finishing its login system.

If you come across any more please let us know via [Discord](http://discord.geysermc.org).

## Which plugin version of Geyser do I need?
This is a non-complete list of what platform each plugin version of Geyser is for, the standalone version can be used for any as it isn't a plugin.
* Geyser-Spigot works with:
  * [Spigot](https://www.spigotmc.org/)
  * [Paper](https://papermc.io/downloads) (recommended)
  * Any other forks of the above
* Geyser-Bungee works with:
  * [BungeeCord](https://www.spigotmc.org/wiki/bungeecord/)
  * [Waterfall](https://papermc.io/downloads#Waterfall)
  * Any other forks of the above
* Geyser-Velocity works with [Velocity](https://www.velocitypowered.com/) *1.1.0 or later*
* Geyser-Sponge works with [SpongeVanilla or SpongeForge](https://www.spongepowered.org/)

## If using BungeeCord or another fork, where do I need to put Geyser/Floodgate?
You only need Geyser and/or Floodgate on the BungeeCord server.

## How can I have Bedrock players load resource packs?

You can add Bedrock resource packs to your Geyser installation in the `packs` folder of wherever the Geyser config is located, and Bedrock clients will automatically download and load those resource packs. This does not add automatic Java-to-Bedrock resource pack conversion, but you can convert any Java resource pack using https://ozelot379.github.io/ConvertJavaTextureToBedrock/ and add that to your server.

## How do I include players in commands when using Floodgate?
If there is a prefix on Floodgate players, the prefix must be included in the name. If this does not work, put double-quotes around the name.

## How do I add players to the whitelist when using Floodgate?
There are two ways you can do this. The first way is to turn off the whitelist using `/whitelist off`, then get the Geyser player to join, then run `/whitelist add "username"`, then turn the whitelist back on using `/whitelist on`. The second way is to add the player's UUID as given by Floodgate to the whitelist.json file and then run `/whitelist reload`.

## How do I find a player's UUID without them joining when using Floodgate?
Use [this page.](https://floodgate-uuid.heathmitchell1.repl.co/) If this doesn't work then try this method:
<br><br>
First, you'll need to get the XUID of the player. There are several third-party websites to find this, for example [this one](https://cxkes.me/xbox/xuid) (unaffiliated with Geyser). Make sure to choose "
Hexidecimal". You'll need to enter the player's Xbox gamertag, and once submitted it should display the XUID in the format of `xxxxxxxxxxxxxxxx`. In order to turn the XUID into a UUID that Java Edition can recognize, you just need to put the XUID in this format: `00000000-0000-0000-xxxx-xxxxxxxxxxxx`. If formatted right, Java Edition should accept it as a UUID.

## Can I use Geyser with Pterodactyl Panel?
Yes, we have an official egg for the standalone version, it supports auto-updating and has all config options easily editable. You can find it [here](https://github.com/GeyserMC/pterodactyl-stuff), just download the JSON egg and import it into your panel.

## Can I use Geyser with Ngrok?
Unfortunately Ngrok is TCP-only, so you will not be able to use Geyser with Ngrok.

## Can I connect Geyser to an older server?
If the server has ViaVersion and/or supports the latest Minecraft version, yes. However at this time we are unable to support older versions of Minecraft due to a limitation in our Java support library.

## Can I use Buycraft with Geyser?
You sure can! Buycraft supports Java & Bedrock players via the Offline store mode **(Recommended to be used with Floodgate)**
### Steps to create a store to support both versions
- Buycraft-> Create Webstore
- Select Game-> Minecraft Offline
- Continue-> Click "Create my Webstore"
- Name your server & Select currency-> Continue
- Select Game Server-> Continue
- Download the plugin version that best suits your server.
- Execute the secret command from your servers console

Your store is now setup to support Bedrock & Java players

**(PLEASE NOTE, BEDROCK PLAYERS MUST INCLUDE THE PREFIX)**

## Can I use CraftingStore with Geyser?
As mentioned above bedrock players must include the prefix in their name
### Steps to make the store work for Geyser
1. Goto the [admin page](https://craftingstore.net/admin)
2. Expand settings on the left
3. Click webshop
4. Make sure 'Require premium accounts' is Off
5. Then if you are using floodgate in each package make sure it uses the player's name in any commands not their UUID

![](https://i.imgur.com/PM7nNSm.png)


## What languages does Geyser support?
We aim to support any of the bedrock languages, see [here](https://translate.geysermc.org/) for our Crowdin page and below is a list of all the language codes.
|Name                        |Code |
|----------------------------|-----|
|Bulgarian                   |bg_bg|
|Czech                       |cs_cz|
|Danish                      |da_dk|
|German                      |de_de|
|Greek                       |el_gr|
|British English             |en_gb|
|American English            |en_us|
|Spanish                     |es_es|
|Mexican Spanish             |es_mx|
|Finnish                     |fi_fi|
|Canadian French             |fr_ca|
|French                      |fr_fr|
|Hungarian                   |hu_hu|
|Indonesian                  |id_id|
|Italian                     |it_it|
|Japanese                    |ja_jp|
|Korean                      |ko_kr|
|Dutch                       |nl_nl|
|Norwegian Bokmål            |nb_no|
|Polish                      |pl_pl|
|Brazilian Portuguese        |pt_br|
|Portuguese                  |pt_pt|
|Russian                     |ru_ru|
|Slovak                      |sk_sk|
|Swedish                     |sv_se|
|Turkish                     |tr_tr|
|Ukrainian                   |uk_ua|
|Chinese Simplified (China)  |zh_cn|
|Chinese Traditional (Taiwan)|zh_tw|
