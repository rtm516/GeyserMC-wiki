With plugins, you can write a program that can do many things! To start, make a plugin.yml, and put it in the main section of a jar file. The format should be:

main: the main class

name: the plugin name

version: the plugin version

Next, you must create a class (the same one which is in "main", in your plugin.yml). It should extend org.geysermc.api.plugin.Plugin. Make use of the many methods in it!