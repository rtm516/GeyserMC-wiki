## Compiling
1. Clone the repo to your computer (EG: `git clone https://github.com/GeyserMC/Geyser.git`)
2. [Install Maven](https://maven.apache.org/install.html)
3. Navigate to the Geyser root directory and run `git submodule update --init --recursive`. This downloads all the needed submodules for Geyser and is a crucial step in this process.
4. Run `mvn clean install` and locate to the `bootstrap`, then your desired Geyser version, then `target` folder.

## IntelliJ
If you're using IntelliJ for editing any of the GeyserMC projects you will most likely need to install the [Lombok](https://plugins.jetbrains.com/plugin/6317-lombok) plugin as it is used to generate a bunch of handy functions. You can edit without it but you may get missing functions and or other issues displayed in IntelliJ.