Commonly, people may have issues with Geyser not showing up in their server list or run into similar issues. This page contains a few common issues people may encounter that you might have as well as potential fixes for them. If you still can't make it work, join [our Discord](https://discord.geysermc.org) for support.

# I can't connect! (Either the server doesn't show up in the friends list or I get "Unable to connect to world")

## If the server doesn't show up in the friends list

* *If using Windows 10, iOS, or Android*: try adding the server to the Servers list in-game.
* *If using Xbox One*: try connecting with [BedrockConnect](https://github.com/GeyserMC/Geyser/wiki/Using-Geyser-with-Consoles).
* *If using PS4*: [try using a LAN proxy.](https://github.com/GeyserMC/Geyser/wiki/Using-Geyser-with-Consoles#playstation-4)
* *If using Nintendo Switch*: there is currently no way for local servers to show up in the Friends tab, but you can still connect using [BedrockConnect](https://github.com/GeyserMC/Geyser/wiki/Using-Geyser-with-Consoles).

*If the Geyser instance is locally hosted:* try using `localhost` or `0.0.0.0` as the IP address. 
*If that doesn't work, or your Geyser instance is on another computer in the network*: use your **local** IPv4 address.

## See [here](https://github.com/GeyserMC/Geyser/wiki/Fixing-%22Unable-to-Connect-to-World%22) for fixing "Unable to Connect to World" with no console errors

### `java.net.BindException: Address already in use: bind` on startup.
This means something (likely another instance of Geyser) is running on the port you have specified in the config. Please make sure you close all applications running on this port. If you don't recall opening anything, usually restarting your computer fixes this. 

### `java.lang.AssertionError: Expected AES to be available` when a user tries to connect

Update your Java at [AdoptOpenJDK.net](https://adoptopenjdk.net/).

### Hosting provider will not immediately open up UDP.

These steps only apply for the standalone version of Geyser.

This usually has something to do on your host's end. Most commonly, it's because they do not open up ports over the UDP protocol, which is what Minecraft: Bedrock Edition uses, opposed to Minecraft: Java Edition using TCP. One way to get around this (if you're using an online host) is to shut down your server, and when asking for a server jar, select Nukkit (you won't actually be switching to Nukkit). Afterward, open up your FTP file manager and find the Nukkit jar. Then, replace this jar with the server software you're using. Upon starting up the server, it should open up ports over UDP whilst still allowing you to use the server jar you desire.

**PLEASE NOTE:** If your server automatically redownloads jars upon startup, such as with an autoupdate system, this workaround will not work. Please contact your host if this does not work for you as there is nothing we can do.

# Login Failed

***If you are using a plugin version:*** in your Geyser config, set your remote address to `127.0.0.1`. If that does not work, check your startup log for a message about Docker, and use that address in the remote address

## Server is in Online Mode while Geyser is in Offline Mode (Access token can not be null or empty)
If you have your configuration set up like this, put simply, it won't work. If authentication for the Java server is set to online, it is expected Geyser is configured the same way. The server requires a valid Minecraft: Java Edition account, and if you aren't logging into one with Geyser, then you will be unable to join the server. If your configuration is set up properly and you're still getting this issue, it could be that your credentials are invalid.

## Connection Refused: <INSERT IP AND/OR DOMAIN>

Connection Refused usually means that a Java server could not be found on that port, or the server denied access to the connection on a network level. The latter can happen with anti-DDOS plugins such as TCPShield, but otherwise ensure that the server you're trying to connect to is spelled correctly in the config, is up and is port forwarded correctly.

If you're updating from an old build of Geyser, set your remote address to `auto` and try again.

## Floodgate Misconfiguration
See [this page](Floodgate) for more information.

## Mojang Resetting Account Credentials
This is unfortunately something we have no control over, and is most likely the case when you're running Geyser as a plugin on a server host or joining a friend far away from your location. If you're running Geyser locally, this should not happen to you, but what we recommend for servers is a plugin we make called [Floodgate](https://github.com/GeyserMC/Floodgate), which allows for Bedrock clients to join your server without needing a Java Edition account. Take a look [here](Floodgate) for more information. 

# "Invalid IP address!" from Bedrock
It's currently unknown why this happens even for valid domains. Try using the IPv4 address.

# Bedrock clients freeze when opening up commands for the first time
Disable `command-suggestions` in your Geyser config. This will stop the freezing at the expense of removing command suggestions from Bedrock clients.

# BungeeCord freezes and crashes after bedrock player joins
Make sure you have set `ip-forward` to `true` in your BungeeCord `config.yml` and set `bungeecord` to `true` in each connected server's `spigot.yml`.

# Failed to load locale asset cache: Unrecognized token 'Cannot'
This or anything else related to failing to download a locale file on startup is usually caused by java trying to connect using IPv6 and Mojang only use IPv4, so start Geyser or the server up with this flag `-Djava.net.preferIPv4Stack=true`, EG: `java -Xms1024M -Djava.net.preferIPv4Stack=true -jar Geyser.jar`

# Outdated client! Please use 1.x.x

The server is too new or Geyser is outdated. Make sure you're on the latest Geyser.

# Outdated server! I'm still on 1.x.x

Update the server or ask them to install ViaVersion.

# Floodgate
For most floodgate issues see: [Floodgate: Known Issues/Caveats](Floodgate#known-issuescaveats).
## If you wish to use IP forwarding, please enable it in your BungeeCord config as well!
It is likely you have enabled `send-floodgate-data` in your Floodgate config but either Floodgate isn't installed on the target server or you floodgate keys aren't the same between the installs of the plugin, please copy them so they all use the same set.