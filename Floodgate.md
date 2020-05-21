Floodgate is a hybrid mode plugin which allows for **Minecraft: Bedrock Accounts** to join **Minecraft: Java Edition** servers without needing a Minecraft: Java Edition account. This is something you install **in addition** to Geyser. Unlike Geyser, Floodgate can **only** be installed as a plugin, and can only be utilized on servers that have it installed. 

[Download](https://ci.nukkitx.com/job/GeyserMC/job/Floodgate/job/development/)

## Setting Up
**NOTE: Floodgate does not replace the Geyser jar. If you are running a plugin version of Geyser, you still MUST have Geyser installed.**

If you are running the plugin versions of Geyser and you have Floodgate installed too, Geyser will automatically detect and load the key, so most of this below should not need to be done. However, if you are running Floodgate on more than one platform (both BungeeCord and Bukkit together for example), you'll need to copy over the keys (as described below) from the platform Geyser is running on. For example, if you are running Geyser on Bukkit, but have Floodgate installed on both BungeeCord and Bukkit, you'll need to copy over the key from the Bukkit version as that's the platform Geyser is running on.

Floodgate currently only works on Bukkit, BungeeCord, and Velocity (using the legacy transfer system). Downloads can be found [here](https://ci.nukkitx.com/job/GeyserMC/job/Floodgate/job/development/). Drag the jar for your platform into the **plugins** folder of your server, and start it up. Upon startup, a file called **public-key.pem** will be generated. **DO NOT DISTRIBUTE THIS KEY TO ANYBODY!** This key is what allows for Bedrock accounts to bypass the Java Edition authentication, and if anyone gets ahold of this, they can wreak havoc on your server. It's not public, despite its name. It's also important security-wise, so nobody can fake being a bedrock client and bypass this system.

Once you find your **public-key.pem**, copy it into the root directory of Geyser, or if you're using the plugin version of Geyser, into your `Geyser` folder found inside of your `plugins` folder (or for Sponge, `config/geyser`). **Make sure** you copy it and don't just drag it. Both Floodgate and Geyser need this file.

In the Geyser config.yml, set `auth-type` to `floodgate`, and restart Geyser. Bedrock clients should now be able to join your Java Edition server without a Java Edition account :D.

## Known Issues/Caveats

## Skins
Due to how Minecraft: Java Edition handles skins, all Bedrock players will appear as Steve or Alex to other Java players. 

## Access token can not be null or empty
This may be because you forgot to set the auth-type in the config to `floodgate`. If that isn't it, check to make sure your config contains the line `floodgate-key-file: public-key.pem`. If not, just copy that in directly.

## Invalid packet id: 27
This usually means one of two things:

* You did not follow the Floodgate instructions properly. However, in an unlikely scenario, this could also be an error related to uploading through FTP. Using ascii will not work here, and you need to make sure you're on binary when uploading.
* You're trying to log in without an Xbox account. Floodgate requires an Xbox account to authenticate the Bedrock player.

## Whitelist command not working
See [this page](FAQ#how-do-i-add-players-to-the-whitelist-when-using-floodgate).

## Obtaining UUIDs for Floodgate players
Check the server log for their UUIDs, or use [this method](FAQ#how-do-i-find-a-players-uuid-without-them-joining-when-using-floodgate).

## Using PlaceholderAPI
If you're using the Bukkit version of Floodgate, download the Placeholder plugin [here](https://github.com/rtm516/FloodgatePlaceholders/). Using the placeholders shouldn't require additional setup other than having [PlaceholderAPI](https://www.spigotmc.org/resources/placeholderapi.6245/) installed.

If you're using the BungeeCord version of Geyser, then you'll need to follow these steps:
+ Edit the floodgate config in your BungeeCord server and enable `send-floodgate-data` in it
+ Then make sure you've enabled `ip_forwarding` in your BungeeCord config.yml and `bungeecord` in your `spigot.yml`
+ Add Floodgate to Spigot server and restart it, then close the server and copy the key file in your BungeeCord server to Spigot server.
+ Then put the placeholder plugin and PlaceholdersAPI in your Spigot server and it should work.

## Using Skript
If you're using the Bukkit version of Floodgate, there is an unofficial plugin that adds Skript support [here](https://github.com/DoctorMacc/floodgate-skript). 