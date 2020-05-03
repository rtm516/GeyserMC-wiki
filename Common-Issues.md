Commonly, people may have issues with Geyser not showing up in their server list or run into similar issues. This page contains a few common issues people may encounter that you might have as well as well as potential fixes for them.

# Geyser Not Showing Up in Server List
This is a _very_ common occurence and is usually one of a few problems nearly every time.

## Loopback Restrictions Not Lifted

_This only affects people trying to join Geyser from Windows 10 Edition with Geyser hosted on the same computer._

This is an issue caused by Loopback restrictions not being lifted. By default, Microsoft Apps have this restriction on all their apps for local connections. You can lift it by typing the following in Windows PowerShell in administrator mode:
```powershell
CheckNetIsolation LoopbackExempt -a -n="Microsoft.MinecraftUWP_8wekyb3d8bbwe"
```

In most cases, Geyser should resolve this issue automatically, but in some events where you may not be an administrator, this will not automatically be resolved.

## Geyser Not Showing Up in Friends Tab
This is also a common one, Geyser won't always show up in your friends tab and you will have to manually add it through the servers tab. Start off by just using `localhost` or `0.0.0.0` as the IP address. If that does not work, use your **local** IPv4 address.

## Geyser Showing Up On Local Computer But Not Anywhere Else

Check your firewall settings and make sure that Java is allowed.

## SRV Records Not Properly Working

Bedrock edition does not support SRV records, so this option won't work at all.

## Using TCP in DNS Options or Portforwarding Instead of UDP

Bedrock uses UDP instead of TCP, so you will have to update your DNS or port forward accordingly if you are using TCP instead.

## Server on External Host Can't Be Connected to Despite Java Players Being able to Connect
This usually has something to do on your host's end. Most commonly, it's because they do not open up ports over the UDP protocol, which is what Minecraft: Bedrock Edition uses, opposed to Minecraft: Java Edition using TCP. One way to get around this (if you're using an online host) is to shut down your server, and when asking for a server jar, select Nukkit (you won't actually be switching to Nukkit). Afterward, open up your FTP file manager and find the Nukkit jar. Then, replace this jar with the server software you're using. Upon starting up the server, it should open up ports over UDP whilst still allowing you to use the server jar you desire.

**PLEASE NOTE:** If your server automatically redownloads jars upon startup, such as with an autoupdate system, this workaround will not work. Please contact your host if this does not work for you as there is nothing we can do.

# Login Failed

## Server is in Online Mode while Geyser is in Offline Mode (Access token can not be null or empty)
If you have your configuration set up like this, put simply, it won't work. If authentication for the Java server is set to online, it is expected Geyser is configured the same way. The server requires a valid Minecraft: Java Edition account, and if you aren't logging into one with Geyser, then you will be unable to join the server. If your configuration is set up properly and you're still getting this issue, it could be that your credentials are invalid.

## Floodgate Misconfiguration
See [this page](Floodgate) for more information.

## Mojang Resetting Account Credentials
This is unfortunately something we have no control over, and is most likely the case when you're running Geyser as a plugin on a server host or joining a friend far away from your location. If you're running Geyser locally, this should not happen to you, but what we recommend for servers is a plugin we make called [Floodgate](https://github.com/GeyserMC/Floodgate), which allows for Bedrock clients to join your server without needing a Java Edition account. Take a look [here](Floodgate) for more information. 
