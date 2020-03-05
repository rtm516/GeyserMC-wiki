# Floodgate

Floodgate is a hybrid mode plugin which allows for **Minecraft: Bedrock Accounts** to join **Minecraft: Java Edition** servers without needing a Minecraft: Java Edition account. This is something you install **in addition** to Geyser. Unlike Geyser, Floodgate can **only** be installed as a plugin, and can only be utilized on servers that have it installed. 


## Setting Up
**NOTE: Floodgate does not replace the Geyser jar. If you are running a plugin version of Geyser, you still MUST have Geyser installed.**

Floodgate currently only works on Bukkit and BungeeCord, and must manually be compiled [here](https://github.com/GeyserMC/Floodgate) using Maven. Once compiled, drag the jar for your platform into the **plugins** folder of your server, and start it up. Upon startup, a file called **public-key.pem** will be generated. **DO NOT DISTRIBUTE THIS KEY TO ANYBODY!** This key is what allows for Bedrock accounts to bypass the Java Edition authentication, and if anyone gets ahold of this, they can wreak havoc on your server. 

Once you find your **public-key.pem**, copy it into the root directory of Geyser, or if you're using the plugin version of Geyser, into your `Geyser` folder found inside of your `plugins` folder (or for Sponge, `config/geyser`). **Make sure** you copy it and don't just drag it. Both Floodgate and Geyser need this file.

In the Geyser config.yml, set `auth-type` to `floodgate`, and restart Geyser. Bedrock clients should now be able to join your Java Edition server without a Java Edition account :D.

## Known Issues/Caveats

## Skins
Due to how Minecraft: Java Edition handles skins, all Bedrock players will appear as Steve or Alex to other Java players. 

## Access token can not be null or empty
This may be because you forgot to set the auth-type in the config to `floodgate`. If that isn't it, check to make sure your config contains the line `floodgate-key-file: public-key.pem`. If not, just copy that in directly.