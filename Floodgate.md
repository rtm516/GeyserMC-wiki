Floodgate is a hybrid mode plugin which allows for **Minecraft: Bedrock Accounts** to join **Minecraft: Java Edition** servers without needing a Minecraft: Java Edition account. This is something you install **in addition** to Geyser. Unlike Geyser, Floodgate can **only** be installed as a plugin on Spigot (including Paper and forks), Bungeecord, and Velocity, and can only be utilized on servers that have it installed. 

[Download](https://ci.nukkitx.com/job/GeyserMC/job/Floodgate/job/development/)

## Prerequisites

- You must own/manage the server in order to add Floodgate. *If you do not own the server, Floodgate does not allow you to bypass logging into Java servers that require a Mojang Java account*.
- The CraftBukkit/Bukkit server software is not supported. Use `floodgate-bukkit` for installing on a Spigot/Paper server.

## Setting Up
**NOTE: Floodgate does not replace the Geyser jar. If you are running a plugin version of Geyser, you still MUST have Geyser installed.**

*Any reference to Spigot here also refers to compatible server softwares such as Paper.*

### Plugin Setup (You have Geyser and Floodgate on the same server)

For multi-server setups: you only are required to install Floodgate on the BungeeCord or Velocity instance unless you want to use the Floodgate API on the other servers - see below for the installation process.

*If using Velocity*: Set `player-info-forwarding-mode` to `LEGACY` in `velocity.toml` 

- Download the Floodgate plugin from [here](https://ci.nukkitx.com/job/GeyserMC/job/Floodgate/job/development/) and add it to your plugins folder on your server (BungeeCord only requires it on the proxy - if you wish to use IP forwarding see below).
- Change the `auth-type` in the Geyser config to `floodgate`.
- Restart/start up the server.

### Standalone Setup (Geyser and Floodgate are in separate places)

- Download the Floodgate plugin from [here](https://ci.nukkitx.com/job/GeyserMC/job/Floodgate/job/development/) and add it to your plugins folder on your server (BungeeCord only requires it on the proxy - if you wish to use IP forwarding see below).
- Run the server with Floodgate.
- *Copy* the `public-key.pem` file in the Floodgate config folder to the same directory as Geyser (standalone) or Geyser's config folder (plugin versions). **DO NOT DISTRIBUTE THIS KEY TO ANYBODY!** This key is what allows for Bedrock accounts to bypass the Java Edition authentication, and if anyone gets ahold of this, they can wreak havoc on your server.
- Change the `auth-type` in the Geyser config to `floodgate`.

### Running Floodgate on Spigot servers behind BungeeCord or Velocity

This is only needed when you want to use the Floodgate API on your Spigot server(s) behind a proxy.

- Download the Floodgate plugin from [here](https://ci.nukkitx.com/job/GeyserMC/job/Floodgate/job/development/) and install it as a plugin on both BungeeCord/Velocity and the Spigot server(s).
- Enable `ip_forwarding` in your BungeeCord `config.yml` if using BungeeCord
- Set `player-info-forwarding-mode` to `LEGACY` in `velocity.toml` if using Velocity
- Set `bungeecord` to `true` in your `spigot.yml`
- Start the proxy server.
- Edit the Floodgate config on your proxy server and set `send-floodgate-data` to `true`.
- *Copy* both key files and the `encrypted.txt` in the Floodgate config folder to Spigot Floodgate's config folder. **DO NOT DISTRIBUTE THIS KEY TO ANYBODY!** This key is what allows for Bedrock accounts to bypass the Java Edition authentication, and if anyone gets ahold of this, they can wreak havoc on your server.
- Restart the Spigot servers and proxy server.

## Account Linking

Floodgate supports account linking, allowing you to join as your Java account on the server. This is an option that can be enabled in the Floodgate config. Once enabled, the steps to link your account are as follows:

- Log in on java and run /linkaccount <xbox gamertag>. 
- You will get a message asking you to run the linkaccount command on Bedrock.
- Run the command given to you, and you will be kicked on Bedrock. Upon relogging, you will be logged in as your java account.

No credentials for either your Java or Bedrock account are needed nor stored in this process.

## Changing/disabling the prefix

***Please note: we do not recommend removing the prefix unless you are certain that no one will share a username between a Java and Bedrock player.***

In your Floodgate config, change `username-prefix` to whichever prefix you desire - you can set it to `""` and there will be no prefix. On Spigot servers, you should also delete your `usercache.json` file located in the same folder as your server jar to prevent users who already joined from having the old prefix.

## Known Issues/Caveats

### Skins
Due to how Minecraft: Java Edition handles skins, all Bedrock players will appear as Steve or Alex to other Java players. 

### Access token can not be null or empty
This may be because you forgot to set the auth-type in the config to `floodgate`. If that isn't it, check to make sure your config contains the line `floodgate-key-file: public-key.pem`. If not, just copy that in directly.

### Invalid packet id: ##
This usually means one of two things:

* You did not follow the Floodgate instructions properly. However, in an unlikely scenario, this could also be an error related to uploading through FTP. Using ascii will not work here, and you need to make sure you're on binary when uploading.
* You're trying to log in without an Xbox account. Floodgate requires an Xbox account to authenticate the Bedrock player.

### java.lang.NumberFormatException: For input string: ""

You're trying to log in without an Xbox account. Floodgate requires an Xbox account to authenticate the Bedrock player.

### Geyser-Floodgate:51777 lost connection: Internal Exception: java.lang.NumberFormatException: For input string: "SfqdXv36" (or a similar error)

Set `ip-forwarding` in your BungeeCord to `true`.

### Whitelist command not working
See [this page](FAQ#how-do-i-add-players-to-the-whitelist-when-using-floodgate).

### Prefix is not changing on the server after changing it in the config.

Ensure that you removed the `usercache.json` file from the server root directory and restart your server.

## Obtaining UUIDs for Floodgate players
Check the server log for their UUIDs, or use [this method](FAQ#how-do-i-find-a-players-uuid-without-them-joining-when-using-floodgate).

## Using PlaceholderAPI
If you're using the Bukkit version of Floodgate, download the Placeholder plugin [here](https://github.com/rtm516/FloodgatePlaceholders/). Using the placeholders shouldn't require additional setup other than having [PlaceholderAPI](https://www.spigotmc.org/resources/placeholderapi.6245/) installed. See the section above on installing Floodgate on backend servers if you wish to use this on BungeeCord.

## Using Skript
If you're using the Bukkit version of Floodgate, there is an unofficial plugin that adds Skript support [here](https://github.com/DoctorMacc/floodgate-skript). 