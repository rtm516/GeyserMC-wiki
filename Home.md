# Geyser
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Build Status](https://ci.nukkitx.com/job/Geyser/job/master/badge/icon)](https://ci.nukkitx.com/job/Geyser/job/master/)
[![Discord](https://img.shields.io/discord/597838753859633172.svg?color=%237289da&label=discord)](https://discord.geysermc.org)

_A bridge between Minecraft: Bedrock Edition and Minecraft: Java Edition._

**Currently supporting MC Bedrock v1.13.X and MC Java v1.14.4.**

The goal of Geyser is to bridge the Minecraft: Bedrock Edition and Minecraft: Java Edition by allowing Bedrock clients to join Java Edition servers. This project is still in development and not complete yet, so expect bugs.

## Setup
Geyser is a **standalone** program, meaning you DO NOT install it as if it were a plugin. It simply works as a proxy, and needs its own directory/configuration files. Bedrock clients will join through Geyser and it will handle all the packet translations.

TehPiggeh does a great job of explaining how to set up Geyser, but if you prefer to read through it yourself, the installation instructions are right below.

[![YouTube Video](https://img.youtube.com/vi/OmLxwl7_UzQ/0.jpg)](https://www.youtube.com/watch?v=OmLxwl7_UzQ)

(If you speak another language, [this page](https://github.com/GeyserMC/Geyser/wiki/Setup-Tutorials) may be helpful as it contains setup videos in different languages)

### Installing
1. Download a jar of Geyser from the [build server](https://ci.nukkitx.com/job/Geyser/job/master/).
2. Create a new folder for Geyser, and drop the jar in there.
3. Create a new bat or startup script, similar to the one you'd use for a Bukkit server, and take a look at [this](https://github.com/GeyserMC/Geyser/wiki/Creating-a-Startup-Script) page for what to put into it.
4. Run the startup script/bat, and all the necessary files for Geyser will be created.
5. Open up Minecraft: Bedrock Edition and in the **Friends** tab, Geyser should show up there. If it does not show up, just add your IPv4 as an external server.

For more information, take a look at the [Setting up the Config]() page, and the [How Geyser Works]() page.

### Plugins
**Please note, Geyser will NOT run any Bukkit, Spigot, BungeeCord or Nukkit plugins!** Geyser has its own plugin API, and if you're interested in developing plugins, take a look at the [Plugin API](https://github.com/GeyserMC/Geyser/wiki/Plugin-API) page.

## Compiling
Geyser uses Maven, so in order to compile it, you will need to install it. Clone the repo, and run `mvn clean install`. Upon compiling, in the **target** folder, you should see a file called `Geyser.jar`. Follow the instructions above if you want to use this rather than the one from the build server.

## Libraries Used
- [NukkitX Bedrock Protocol Library](https://github.com/NukkitX/Protocol)
- [Steveice10's Java Protocol Library](https://github.com/Steveice10/MCProtocolLib)
- [TerminalConsoleAppender](https://github.com/Minecrell/TerminalConsoleAppender)
- [Simple Logging Facade for Java (slf4j)](https://github.com/qos-ch/slf4j)