# [Download here](https://ci.nukkitx.com/job/GeyserMC/job/Geyser-Fabric/job/java-1.16/lastSuccessfulBuild/artifact/build/libs/Geyser-Fabric-1.0-SNAPSHOT.jar)

For the most part, Geyser-Fabric operates the same as other Geyser platforms. There are a couple of exceptions:

- Geyser-Fabric is installed in the `mods` folder, and its config can be found in `config/Geyser-Fabric/config.yml` at the root of your server.
- Any mod that requires clientside installation in order to join the server will not permit Bedrock clients to join.
- Floodgate is currently not supported on Fabric.
- You must install the Fabric API mod from [here](https://www.curseforge.com/minecraft/mc-mods/fabric-api).

### permissions.yml

This file located in `config/Geyser-Fabric` controls what commands non-opped players (both Bedrock and Java) are able to run. Uncomment the desired commands.

### Why a separate repository?

- By maintaining a separate repository, we can support multiple Minecraft versions easier.
- Fabric is built around the Gradle build tool, while Geyser is built around the Maven build tool.