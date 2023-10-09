# crucial2_container
# Run crucial 2 modpack minecraft server on a docker container!

1) Modify volume path to map the container host directory to the data directory within the container
2) Some mods have restrictions that don't allow dl. Manually Move Mirabilis jar to mods folder in container (may be able to include this in the repo and include that copy command in the docker compose) MAke sure the name matches what the server expects
3) Restart container so it picks up that mod it couldn't dl
4) Profit
