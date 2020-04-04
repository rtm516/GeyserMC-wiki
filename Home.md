# Geyser
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Build Status](https://ci.nukkitx.com/job/Geyser/job/master/badge/icon)](https://ci.nukkitx.com/job/Geyser/job/master/)
[![Discord](https://img.shields.io/discord/613163671870242838.svg?color=%237289da&label=discord)](https://discord.geysermc.org)

_A bridge between Minecraft: Bedrock Edition and Minecraft: Java Edition._

**Currently supporting MC Bedrock v1.14.X and MC Java v1.15.2.**

The goal of Geyser is to bridge the Minecraft: Bedrock Edition and Minecraft: Java Edition by allowing Bedrock clients to join Java Edition servers. This project is still in development and not complete yet, so expect bugs.

## Setup
Bedrock clients will join through Geyser and it will handle all the packet translations. There are four different versions of Geyser: Geyser for Bukkit (works on derivatives such as Spigot and Paper), Geyser for BungeeCord (also works on Waterfall), Geyser for Velocity, and Geyser Standalone. The first three versions run as plugins, and can be installed directly onto the server. The standalone version can be used in a similar way, except you run it separately. 

If you are running a server, it is highly recommended you use one of the plugin versions, and if you want to join a server that does not have Geyser installed, you can run the standalone version. 

## Installing
### Standalone
1. Download a jar of Geyser from the [build server](https://ci.nukkitx.com/job/Geyser/job/master/).
2. Create a new folder for Geyser, and drop the jar in there.
3. Create a new bat or startup script, similar to the one you'd use for a Bukkit server, and take a look at [this](https://github.com/GeyserMC/Geyser/wiki/Creating-a-Startup-Script) page for what to put into it.
4. Run the startup script/bat, and all the necessary files for Geyser will be created.
### Plugin
1. Download a jar of Geyser from the [build server](https://ci.nukkitx.com/job/Geyser/job/master/) depending on what platform your server runs on.
2. Put Geyser in your plugins folder and start up the server.
3. Configure any needed options in the Geyser config. In most scenarios this file should not need to be touched unless you intend to use [Floodgate](https://github.com/GeyserMC/Geyser/wiki/Floodgate), or you're running your Java on a port that is not 25565.
4. Restart your server if needed.

Once you're done, open up Minecraft: Bedrock Edition and in the **Friends** tab, Geyser should show up there. If it does not show up, just add your IPv4 as an external server. 

If you're still having problems with Geyser not working or giving you an "Unable to connect to world" error, see the [Common Issues](https://github.com/GeyserMC/Geyser/wiki/Common-Issues) page.

For more information, take a look at the [Understanding the Config](https://github.com/GeyserMC/Geyser/wiki/Understanding-the-Config) page, and the [How Geyser Works](https://geysermc.org/#howitworks) page.

## How Does it Work?
Geyser works as a translator, translating both the incoming and outgoing packets to a format both the client and server can understand. With this being said, it emulates a Minecraft: Java Edition client, so the server actually thinks you're joining from Java Edition. Regardless of the server or what plugins it has installed, you can join it with Geyser (as long as the server supports the latest Minecraft version).

## Compiling
Geyser uses Maven, so in order to compile it, you will need to install it. Clone the repo, and run `mvn clean install`. Upon compiling, in the **target** folder, you should see a file called `Geyser.jar`. Follow the instructions above if you want to use this rather than the one from the build server.