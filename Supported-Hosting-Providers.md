This list is incomplete. Please add a link or contact us on Discord if the information is incorrect or you want to add a new hosting provider!

It should also be noted that these providers may not be verified by the Geyser team, and the server providers below are reported as working by members of the community.

**Warning: The below information is for the plugin versions of Geyser unless otherwise specified**

## Built-in Geyser
* [Aternos](https://aternos.org/) (Select as a plugin in the Aternos plugin list and connect to your server with your Java IP and port. See [Aternos's article](https://support.aternos.org/hc/en-us/articles/360051047631) for more details.)
* [CreeperHost](https://www.creeperhost.net/) (Has a toggle within the control panel to automatically enable Geyser. May not be enabled by default, so you may need to toggle it and restart the server)
* [MCProHosting](https://mcprohosting.com/) (Click "Enable Bedrock Support" on your OneControlCenter server dashboard and follow the steps. To host your own: Add 19132 UDP to the [port forward mapping](https://clients.mcprohosting.com/index.php?rp=/knowledgebase/379/Firewall-and-Port-Management.html) and connect to the given source port)
* [Minehut](https://minehut.com/) (Connect via `bedrock.minehut.com` and do `/join <servername>`.)
* [SRKHOST](https://www.srkhost.eu/) (You can enable Geyser at the Version changer page, this feature is built-in and uses the given port by the host.)

## Support for Geyser
* [Akliz](https://www.akliz.net/) (They should have a port forwarding option that works)
* [Apex Hosting](https://apexminecrafthosting.com/) (Need to set the Bedrock address in the config on the Java IP, default port may not work)
* [Aquatis](https://aquatis.host/) (Need to open a support ticket to get UDP ports and then update the config to reflect your new Bedrock port)
* [Azure](https://azure.microsoft.com/) (Not a dedicated Minecraft provider; set your Bedrock address in your config to `127.0.0.1`.)
* [BisectHosting](https://www.bisecthosting.com/) (Need to ask to open a UDP port, and set the Bedrock address in the config to the Java IP)
* [Bloom.Host](https://www.bloom.host/) (Can use 25565 port for Bedrock, or you can make a ticket to open a 19132 port)
* [Dashflo.net](https://dashflo.net/) (Use the same port as your Java server for the Bedrock port in your config and connect with that port, or buy a dedicated IP address to support different port)
* [Century-Hosting](https://century-hosting.com) (**The things at Century Hosting are not going so great, Untested basically.**)
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
* [GGServers](https://ggservers.com/) (Requires a Bedrock node. Use the same address and port as your Java server for the Bedrock address and port in your config and connect with that port.)
* [Google Cloud](https://cloud.google.com/) (Not a dedicated Minecraft provider)
  - 90 day/$300 free trial
  - [Tutorial for a Minecraft server Google Cloud](https://cloud.google.com/solutions/gaming/minecraft-server)
  - Note: You'll need to also allow port 19132 on UDP, use Paper instead of vanilla and put Geyser in the plugins folder
  - You also don't need an SSD, they're just trying to make you pay more
* [Heavynode](https://www.heavynode.com/) (Use default port and 0.0.0.0 as address. 19132 is blocked for DDOS reasons so your best bet is to use the same port as your Java server for the Bedrock port in your config and connect with that port)
* [Hetzner](https://hetzner.com) (Not a dedicated Minecraft provider)
* [HumbleServers](https://humbleservers.com/) (Use the same port as your Java server for the Bedrock port in your config, or one of the two extra ports, and connect with that port. If the subdomain doesn't work, use your regular ip address with numbers.)
* [Meloncube](https://www.meloncube.net/) (Need to ask to open a UDP port)
* [MineStrator](https://minestrator.com/) (Use the same port as your Java server for the Bedrock port in your config and connect with that port)
* [NiCraft](https://www.ni-host.com/)
  - Use the same port as your Java server for the Bedrock port in your config and connect with that port.
  - See [here](https://github.com/GeyserMC/Geyser/wiki/Common-Issues#bedrock-players-can-connect-after-hitting-the-server-on-a-tcp-port-eg-on-java-or-a-website-on-the-same-server)
  - So if your players encounter this issue, please ask them to try to connect (even if they don't have Minecraft) from Java Edition first while their Bedrock client is opened and after they should be able to join on Bedrock Edition.
* [OVH](https://www.ovh.com/) (Not a dedicated Minecraft provider)
* [Pebblehost](https://pebblehost.com/) (Use the same port as your Java server for the Bedrock port in your config and connect with that port)
* [PhoenixNodes](https://phoenixnodes.com) (Open a ticket to request an additional port for Geyser)
* [RamShard](https://ramshard.com/) (Use the same port as your Java server for the Bedrock port in your config and connect with that port)
* [Revivenode](https://revivenode.com/) (Use the same port as your Java server for the Bedrock port in your config and connect with that port)
* [ScalaCube](https://scalacube.com/) (Use the same address and port as your Java server for the Bedrock address and port in your config and connect with that port)
* [Server.pro](https://server.pro) (Use the same port as your Java server for the Bedrock port in your config and connect with that port; enable the `clone-remote-port` option if using the free plan; don't use the docker IP.)
* [Shockbyte](https://shockbyte.com/) (Use the same IP and port as your Java server for the Bedrock address and port in your config and connect with that port. You can also see standalone installation instructions [here](https://shockbyte.com/billing/knowledgebase/173/Introduction-to-GeyserMCorDragonProxy-How-GeyserMC-Works.html).)
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
* [Hicoria](https://hicoria.com/en/) (Only way to run Geyser is to buy VPS or "MC Ultimate" (thats VPS with easier way to run .jars) and run standalone version there.)
* [MCPEhost](https://mcpehost.ru/)
* [MyArena](https://www.myarena.ru/) (Does seem to be working, but the java version is too old in order for Geyser to run properly)
* [NFOservers](https://nfoservers.com/) (As an alternative, you can run Geyser standalone separately)
* [PloudOS](https://ploudos.com/)
