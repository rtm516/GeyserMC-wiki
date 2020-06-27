## Setup
(For GeyserConnect to work you need 2 UDP ports open, by default these are `19132` and `19133`.)
1. Download the latest build from [Jenkins](https://ci.nukkitx.com/job/GeyserMC/job/GeyserConnect/job/master/)
2. Edit the config as needed
3. Start the server as you do with a normal Geyser install. EG: `java -Xms1024M -jar GeyserConnect.jar` (More info on [Creating a Startup Script](Creating-a-Startup-Script))
4. Connect to it to make sure its all working.

## DNS and Docker
There are both [DNS](https://github.com/GeyserMC/GeyserConnect/tree/master/bind9) (using bind9) and [Docker](https://github.com/GeyserMC/GeyserConnect/tree/master/docker) configs in the repo if you would like to use them.

## Config
* `address` - The IP address that will listen for connections.
* `remote-address` - The IP address to forward players to, this needs to be accessible by the client. Set it to `auto` to grab your public IP automatically.
* `port` - The port that will listen for connections.
* `debug-mode` - If debug messages should be sent through console.
* `max-players` - Maximum amount of players that can connect.
* `motd` - MOTD to display.
* `geyser`
  * `port` - The port that will listen for connections.
  * `debug-mode` - If debug messages should be sent through the console, has to be enabled in both places to work.
  * `shutdown-time` - The time to wait after the last player disconnects to shutdown the proxy, in seconds. Set to -1 to disable.
* `servers` - A list of servers to show for everyone build from `address`, `port`, `online` and `bedrock` all optional apart from address.
* `custom-servers`
  * `enabled` - Should custom servers be enabled for users.
  * `max` - Max amount of custom servers per user.
  * `storage-type` - Storage engine for custom servers. Can be `json`, `sqlite`, `mysql`
  * `mysql` - Connection information for the MySQL database if enabled

The default config can be found [here](https://github.com/GeyserMC/GeyserConnect/blob/master/src/main/resources/config.yml).

