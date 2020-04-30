**This covers setting up Geyser Standalone for Android using Termux. If you are just wanting Android support then use any of the gides as Geyser supports Android regardless on how it runs**
1. Go to [here](https://ci.nukkitx.com/job/GeyserMC/job/Geyser/job/master/) and access the latest build. Copy the download address of the jar that fits your server and `wget` it into your `plugins` folder on the server. 
2. Go to [here](https://ci.nukkitx.com/job/GeyserMC/job/Floodgate/job/development/) and access the latest build. Copy the download address of the download that fits your server and `wget` it into your `plugins` folder as well.  
3. Start the server and wait for it to finish loading. 
4. Stop the server.  
5. Navigate to your `plugins` folder. 
6. Enter the folder that has a name starting with floodgate. 
7. Move the `public-key.pem` file into the folder that was created which has a name starting with Geyser. 
8. In the same Geyser folder, use `nano` to edit the `config.yml` file and change the `auth-type` to floodgate. 
9. Head back to [here](https://ci.nukkitx.com/job/GeyserMC/job/Geyser/job/master/) and copy the download address of the version of Geyser that is simply named `Geyser.jar`. 
10. Create a folder on the root of your minecraft server and navigate to it. 
11. Use `wget` to get `Geyser.jar` into the folder. 
12. Run it using `java -jar Geyser.jar` 
13. Once Geyser is done loading hit `CTRL+C `
14. Use `nano` to edit the `config.yml` file that was created in the folder. Change the port it is listening on to 19134. 
15. Run `tmux new-session -s geyser` 
16. Run `java -jar Geyser.jar` 
17. Detach from tmux.  
18. Navigate to your minecraft root folder. 
19. Run `tmux new-session -s server` 
20. Start your server 
21. You are done! Now to have players connect without a java account from bedrock have them set their port to 19132. If they have a java account get them to set it to 19134. If they are on pc java edition then no port is required.