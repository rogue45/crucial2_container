# crucial2_container
# Run crucial 2 modpack minecraft server on a docker container!

# Server side setup
1) Create a curseforge account and login
2) Open a tab to https://console.curseforge.com and get an api key
3) Update the api key in the docker compose to your value (IMPORTANT: Place an additional $ before any existing $ in the key. ie $ becomes $$)
4) Modify volume path to map a container host directory to the data directory within the container. You want your data stored on a host volume to prevent restarts from wiping your world data.
5) Start the container. It will generate a file that contains the list of things it couldn't download (Some mods have restrictions that don't allow dl)
6) Manually Move Mirabilis jar to mods folder in container using winscp(windows) or scp(mac/linux) // I should be able to script this in the future as part of the docker compose
7) Restart container so it picks up that mod it couldn't dl
8) Profit

Notes: The exclusions in the docker compose remove client side mods from getting installed on the server.



# Client side. 
1) In the windows xbox minecraft launcher i installed the older flavor of minecraft 1.16.5.
2) Opened overwolf and installed crucial 2.
3) Opened minecraft launcher and launched the crucial 2.
4) Clicked multiplayer and entered in the local ip of my container host 192.168.1.?
5) Enjoy
