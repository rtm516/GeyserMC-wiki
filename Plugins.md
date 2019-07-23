### Basics
With plugins, you can write a program that can do many things! To start, make a plugin.yml, and put it in the main section of a jar file. The format should be:

main: the main class

name: the plugin name

version: the plugin version

Next, you must create a class (the same one which is in "main", in your plugin.yml). It should extend org.geysermc.api.plugin.Plugin. Make use of the many methods in it!

### Logging
Logging in geyser uses the a new implementation, Geyser.getLogger().

GeyserLogger methods:
The geyser logger has many methods to use.

debug: sends a gray debug message, that usually no one should have to see

info: sends a white info message, that may contain something useful

warning: sends a yellow warning that something may be wrong

error: sends a red message, meaning that something needs to be fixed, your program cannot function

severe: a fatal error has occurred. This method marks it's text in dark red


If the colors in those methods aren't enough, use the ColoredConsole and ChatColor classes.

### Events
Events let you run methods when something happens. To do so, you must make your listener implement the Listener class, and then register it in the PluginManager. To add an event, you must make a public method, with any name, and annotate it with the @EventHandler annotation. Any object may be used as an event. To run an event, use the PluginManager#runEvent() method.
Example:
`public void onPing(PingEvent event) {
    GeyserLogger.DEFAULT.info("Recieved ping!");
 }
`

