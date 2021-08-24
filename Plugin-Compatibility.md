This list is incomplete. Please add a link or contact us on Discord if the information is incorrect or you want to add a new hosting provider!

For compatibility with anticheat plugins, please see [Anticheat Compatibility](https://github.com/GeyserMC/Geyser/wiki/Anticheat-Compatibility)

If a plugin you have is not listed, consider it compatible unless you discover otherwise.
If you come across any more, please let us know via [Discord](http://discord.geysermc.org).

## Incompatible

Geyser should generally work fine with plugins, as we emulate a Java client. There are exceptions, though:

Floodgate can cause issues with plugins as it modifies the login process. *Please note that any offline mode authenticator plugins are only here for documentation; Geyser does not support offline mode usage.*

* [DynamicBungeeAuth](https://www.spigotmc.org/resources/dynamicbungeeauth-premium-command-semi-premium-system-sessions.27480/) produces invalid credentials for Bedrock players.
* [FastLogin](https://www.spigotmc.org/resources/fastlogin.14153/) does not let floodgate add player prefix.
* [ExploitFixer](https://www.spigotmc.org/resources/2ls-exploitfixer-the-ultimate-antiexploit-plugin.62842/) thinks that Floodgate users are UUID spoofing - disable the `uuidspoof` setting in ExploitFixer's config.
* [JPremium](https://www.spigotmc.org/resources/27766/) alters the UUID of a player, causing Floodgate not to be able to get the Bedrock data from its map.
* [LibHatesMods](https://www.spigotmc.org/resources/78202/) causes authentication to fail with `com.github.steveice10.mc.auth.exception.request.InvalidCredentialsException`
* ~~[ProtocolSupport](https://www.spigotmc.org/resources/7201/) sometimes causes issues with Floodgate saying `Invalid packet id: 27`. Use [ViaVersion](https://www.spigotmc.org/resources/19254/) instead if this keeps occurring~~ ProtocolSupport now works with the latest Floodgate.
* [ProtocolSupportBungee](https://www.spigotmc.org/resources/8733/) changes how the login process works and therefore breaks the floodgate injection code.
* [SayNoToMcLeaks](https://www.spigotmc.org/resources/40906/) prevents Floodgate from finishing its login system.

## Compatible with changes

* [TCPShield](https://tcpshield.com/) requires `only-allow-proxy-connections` disabled without a paid plan. However, their "Premium" plan will allow the support of Geyser - please contact their support for help setting this up. 