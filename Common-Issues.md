# Common Issues

Commonly, people have issues with Geyser not showing up in their server list or run into similar issues. This page contains a few common issues people may encounter that you might have as well.

## Geyser Not Showing Up in Server List
This is a _very_ common occurence and is usually one of a few problems nearly every time.

### Loopback Restrictions Not Lifted

_This only affects people trying to join Geyser from the same computer it's hosted on_

This is an issue caused by Loopback restrictions not being lifted. By default, Microsoft Apps have this restriction on all their apps for local connections. You can lift it by typing the following in Windows PowerShell in administrator mode:
```powershell
CheckNetIsolation LoopbackExempt -a -n="Microsoft.MinecraftUWP_8wekyb3d8bbwe"
```

### Geyser Not Showing Up in Friends Tab

This is also a common one, Geyser won't always show up in your friends tab and you will have to manually add it through the servers tab. Start off by just using `localhost` or `0.0.0.0` as the IP address. If that does not work, use your **local** IPv4 address.

### SRV Records Not Properly Working

Bedrock edition does not support SRV records, so this option won't work at all.

### Using TCP in DNS Options Instead of UDP

Bedrock uses UDP instead of TCP, so you will have to update your DNS accordingly if you are using TCP. 