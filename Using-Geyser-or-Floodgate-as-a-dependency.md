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
    <version>1.4.3-SNAPSHOT</version>
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

This page has a very simple primer for the Floodgate API. For a full breakdown, see [here](https://github.com/GeyserMC/Floodgate/wiki/FloodgateApi).

Add Floodgate's API as a dependency:
```xml
<dependency>
    <groupId>org.geysermc.floodgate</groupId>
    <artifactId>api</artifactId>
    <version>2.0-SNAPSHOT</version>
    <scope>provided</scope>
</dependency>
```

Get the Floodgate API using:
```java
FloodgateApi api = FloodgateApi.getInstance();
api.isFloodgatePlayer(uuid);
```