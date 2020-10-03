This list is incomplete. Please add a link or contact us on Discord if the information is incorrect or you want to add a new hosting provider!

It should also be noted that these providers may not be verified by the Geyser team, and the server providers below are reported as working by members of the community.

**Warning: The below information is for the plugin versions of Geyser unless otherwise specified**

## Built-in Geyser
* [Minehut](https://minehut.com/) (Connect via `bedrock.minehut.com` and do `/join <servername>`. **Please note: Minehut currently has a bug where any Bedrock player cannot interact with the world. The current workaround is to switch gamemodes when you log into your server.**)
* [CreeperHost](https://www.creeperhost.net/) (Has a toggle within the control panel to automatically enable Geyser. May not be enabled by default, so you may need to toggle it and restart the server)

## Support for Geyser
* [Akliz](https://www.akliz.net/) (They should have a port forwarding option that works)
* [Apex Hosting](https://apexminecrafthosting.com/) (Need to set the Bedrock address in the config on the Java IP, default port may not work)
* [Aquatis](https://aquatis.host/) (Need to open a support ticket to get UDP ports and then update the config to reflect your new Bedrock port)
* [Azure](https://azure.microsoft.com/) (Not a dedicated Minecraft provider; set your Bedrock address in your config to `127.0.0.1`.)
* [BisectHosting](https://www.bisecthosting.com/) (Need to ask to open a UDP port, and set the Bedrock address in the config to the Java IP)
* [BloomVPS](https://www.bloomvps.com/) (Can use 25565 port for Bedrock, or you can make a ticket to open a 19132 port)
* [Dashflo.net](https://dashflo.net/) (Use the same port as your Java server for the Bedrock port in your config and connect with that port, or buy a dedicated IP address to support different port)
* [CentryHosting](https://century-hosting.com) (Use the same port as your Java server for the Bedrock port in your config and connect with that port)
* [Craft-Hosting](https://craft-hosting.ru/) (Use the same port as your Java server for the Bedrock port in your config and connect with that port; note that this provider appears to only provide service in Russia.)
* [DedicatedMC](https://dedicatedmc.io/) (Need to ask to open the default bedrock port.)
* [ExtraVM](https://extravm.com/) (Not a dedicated Minecraft provider)
* [Easly](https://easlyhost.com) (Use the same port as your Java server for the Bedrock port in your config and connect with that port)
* [FadeHost](https://fadehost.com/) (Use the same port as your Java server for the Bedrock port in your config and connect with that port or buy a dedicated IP address to support different port)
* [FalixNodes](https://falixnodes.net/) (Use the same port as your Java server for the Bedrock port in your config and connect with that port)
* [Ferox Hosting](https://feroxhosting.nl) (Open a ticket to request a UDP port)
* [FreeMC.Host](https://freemc.host/) (Use the same port as your Java server for the Bedrock port in your config and connect with that port)
* [FreeMcServer.net](https://freemcserver.net) (Use the same port as your Java server for the Bedrock port in your config and connect with that port)
* [GameHosting.it](https://www.gamehosting.it/) (Use the same port as your Java server for the Bedrock port in your config and connect with that port)
* [GameHosting.gg](https://gamehosting.gg/) (Use the same port as your Java server for the Bedrock port in your config and connect with that port)
* [Gamers Hosting](https://gamershosting.ga/) (Open a ticket to request a UDP port or Use the same port as your Java server for the Bedrock port in your config and connect with that port)
* [GGServers](https://ggservers.com/) (Requires a Bedrock node [Unknown if you still need one])
* [Google Cloud](https://cloud.google.com/) (Not a dedicated Minecraft provider)
  - 1 year/$300 free trial
  - [Tutorial for a Minecraft server Google Cloud](https://cloud.google.com/solutions/gaming/minecraft-server)
  - Note: You'll need to also allow port 19132 on UDP, use Paper instead of vanilla and put Geyser in the plugins folder
  - You also don't need an SSD, they're just trying to make you pay more
* [Heavynode](https://www.heavynode.com/) (Use default port and 0.0.0.0 as address. 19132 is blocked for DDOS reasons so your best bet is to use the same port as your Java server for the Bedrock port in your config and connect with that port)
* [Hetzner](https://hetzner.com) (Not a dedicated Minecraft provider)
* [HumbleServers](https://humbleservers.com/) (Use the same port as your Java server for the Bedrock port in your config, or one of the two extra ports, and connect with that port. If the subdomain doesn't work, use your regular ip address with numbers.)
* [MCProHosting](https://mcprohosting.com/) (Click "Enable Bedrock Support" on your OneControlCenter server dashboard and follow the steps, modded servers not supported)
* [Meloncube](https://www.meloncube.net/) (Need to ask to open a UDP port)
* [MineStrator](https://minestrator.com/) (Use the same port as your Java server for the Bedrock port in your config and connect with that port)
* [OVH](https://www.ovh.com/) (Not a dedicated Minecraft provider)
* [Pebblehost](https://pebblehost.com/) (Use the same port as your Java server for the Bedrock port in your config and connect with that port)
* [PhoenixNodes](https://phoenixnodes.com) (Open a ticket to request an additional port for Geyser)
* [RamShard](https://ramshard.com/) (Use the same port as your Java server for the Bedrock port in your config and connect with that port)
* [Revivenode](https://revivenode.com/) (Use the same port as your Java server for the Bedrock port in your config and connect with that port)
* [ScalaCube](https://scalacube.com/) (Use the same address and port as your Java server for the Bedrock address and port in your config and connect with that port)
* [Server.pro](https://server.pro) (Use the same port as your Java server for the Bedrock port in your config and connect with that port; enable the `clone-remote-port` option if using the free plan; don't use the docker IP.)
* [Shockbyte](https://shockbyte.com/) (Use the same port as your Java server for the Bedrock port in your config and connect with that port. You can also see standalone installation instructions [here](https://shockbyte.com/billing/knowledgebase/173/Introduction-to-GeyserMCorDragonProxy-How-GeyserMC-Works.html).)
* [Skynode.pro](https://skynode.pro/)
  - Use the port provided by Skynode
  - Only Geyser Standalone can be used
  - You'll need to make a new server to host Geyser on
  - Replace the server.jar with the Geyser.jar (from [Jenkins](https://ci.nukkitx.com/job/GeyserMC/job/Geyser/job/master/))
* [SoYouStart](https://www.soyoustart.com) (See [here](https://github.com/GeyserMC/Geyser/wiki/Common-Issues#bedrock-players-can-connect-after-hitting-the-server-on-a-tcp-port-eg-on-java-or-a-website-on-the-same-server))
* [Sparked Host](https://sparkedhost.com) (Use the same port as your Java server for the Bedrock port in your config and connect with that port)
* [SpawnMC](https://spawnmc.net/) (Use the same port as your Java server for the Bedrock port in your config and connect with that port; note that this provider only provides service in China)
* [STIPE](https://stipe.com.au/) (Use the same port as your Java server for the Bedrock port in your config and connect with that port; note that this provider only provides service in Australia)
* [The Minecraft Hosting](https://theminecrafthosting.com/) (19132 should work as a Bedrock port, if not use the same port as your Java server for the Bedrock port in your config and connect with that port)
* [Titan Nodes](https://titannodes.com/) (Use the Default server port and 0.0.0.0 as the host address.)
* [TNAHosting](https://tnahosting.net/) (Use the same port as your Java server for the Bedrock port in your config and connect with that port)
* [WinterNode](https://winternode.com) (Use the same port as your Java server for the Bedrock port in your config and connect with that port, request an additional port, or buy a dedicated IP address)
* [Witherhosting](https://witherhosting.com/) (Use the same port as your Java server for the Bedrock port in your config and connect with that port)
* [ZapHosting](https://zap-hosting.com/en/) (Use the same port as your Java server for the Bedrock port in your config and connect with that port, request an additional port, or buy a dedicated IP address)

## Does not support Geyser
* [Aternos](https://aternos.org/) (As an alternative, you can run Geyser standalone separately)
* [Hicoria](https://hicoria.com/en/) (Only way to run Geyser is to buy VPS or "MC Ultimate" (thats VPS with easier way to run .jars) and run standalone version there.)
* [MCPEhost](https://mcpehost.ru/)
* [MyArena](https://www.myarena.ru/) (Does seem to be working, but the java version is too old in order for Geyser to run properly)
* [PloudOS](https://ploudos.com/)