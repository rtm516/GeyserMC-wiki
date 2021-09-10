To start, add the Open Collaboration repository to your project:

```xml
<repository>
    <id>opencollab-snapshot-repo</id>
    <url>https://repo.opencollab.dev/maven-snapshots/</url>
    <releases>
        <enabled>false</enabled>
    </releases>
    <snapshots>
        <enabled>true</enabled>
    </snapshots>
</repository>
```

## Using Geyser

Add Geyser's common codebase as a dependency:

```xml
<dependency>
    <groupId>org.geysermc</groupId>
    <artifactId>connector</artifactId>
    <version>1.2.1-SNAPSHOT</version>
    <scope>provided</scope>
</dependency>
```

To get a Geyser player, or check if a player is from Bedrock:

```java
GeyserSession session = GeyserConnector.getInstance().getPlayerByUuid(uuid);
```

`session` can be null if such a player does not exist on Geyser.

`GeyserConnector.getInstance()` will be null until after the Geyser plugin enables.


## Using Floodgate

See https://github.com/Camotoy/floodgate-skript/blob/master/pom.xml as a reference for now; this documentation will later be updated for Floodgate 2.0.
Add floodgate's API as a dependency:
```xml
<dependency>
    <groupId>org.geysermc.floodgate</groupId>
    <artifactId>api</artifactId>
    <version>2.0-SNAPSHOT</version>
    <scope>provided</scope>
</dependency>
```

Get floodgate API using:
```java
FloodgateApi api = FloodgateApi.getInstance();
api.isFloodgatePlayer(uuid);
```
Floodgate API supports many more features, for complete documentation of floodgate api, see [this](https://github.com/GeyserMC/Floodgate/wiki/FloodgateApi).