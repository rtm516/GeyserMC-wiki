*Unable to Connect to World* is by far the most common error people get when attempting to set up Geyser. Here's some steps on how to solve that.

# Before we start...

## ...Java players can't connect either!

This **should not be** a Geyser problem. Geyser does not modify server behavior. Floodgate does modify the login structure but only for Bedrock players. Contact your hosting provider or look elsewhere for fixing this connection issue.

## ...I just updated, and now it doesn't work!

If this occurred after updating a plugin version of Geyser, ensure that you shut off your server, swapped the Geyser jar, and then started up your server.

## ...There are errors in my console!

Please read through the [common issues page](https://github.com/GeyserMC/Geyser/wiki/Common-Issues). If there is another error not documented there, join us on our [Discord](https://discord.geysermc.org).

## ...Have you tried restarting?

Especially on mobile devices, sometimes just restarting Minecraft fixes the issue.

# General troubleshooting steps

## Using TCP in DNS options/port forwarding Instead of UDP

Minecraft: Java Edition uses TCP for connecting; Minecraft: Bedrock Edition uses UDP. Specifying `TCP/UDP` should also work but is not recommended.

## Bedrock port is less than 10000

Historically, having a Bedrock port that is a lower number will cause issues. Setting it to 10000 or above seems safe.

## Bedrock players can connect *after* hitting the server on a TCP port (e.g. on Java or a website on the same server)

This is likely a firewall issue on your server. 

Here is how to prevent the issue on SoYouStart (a subsidiary of OVH):

In the SoYouStart control panel:
1. Click the IP tab.
2. Click the gear at the right of the public IP address; select "Game mitigation".
3. Pick "Add a rule".
4. Select "minecraftPocketEdition" in the dropdown list and enter the target UDP ports.
5. Save and wait a few seconds for the changes to come into effect.

## Changing the `bedrock` `address` in the Geyser config.

Except for a few specific hosting providers, you generally do not need to change this part of the Geyser config. However, in rare instances, it does fix issues

# Using a hosting provider or other location

## Read me first!!!

Many providers and remote hostings have additional steps you have to perform in order to be supported; see [Supporting Hosting Providers](https://github.com/GeyserMC/Geyser/wiki/Supported-Hosting-Providers). If you're self-hosting from home, you don't need to worry about this.

## Pterodactyl

If you get this error while using the Pterodactyl Panel, try editing the Geyser config and changing the port to something besides `19132` (e.g. `25566`).

## Hosting Geyser on another computer on the same network

### Can only connect from the same computer and not anywhere else

Your firewall is likely in the way. Try adding an exception to Java, or disable the firewall for testing purposes.

# Using Geyser on the same computer

## Windows 10

_This only affects people trying to join Geyser from Windows 10 Edition with Geyser hosted on the same computer._

This is an issue caused by Loopback restrictions not being lifted. By default, Microsoft Apps have this restriction on all their apps for local connections. Geyser will attempt to resolve this automatically; however, if you're still having connection problems, you can lift it by typing the following in Windows PowerShell in administrator mode: (it should return `OK.` if it worked)
```powershell
CheckNetIsolation LoopbackExempt -a -n="Microsoft.MinecraftUWP_8wekyb3d8bbwe"
```

