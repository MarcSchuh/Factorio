# Factorio

This repository contains a small Docker Compose setup for running Factorio.

## Prerequisites

1. Make sure you have Docker Compose version 2.0 or higher.  
2. Ensure the "data" folder in your project directory has the owner 845:845:  
   ```bash
   sudo chown -R 845:845 data
3. Open the necessary ports in your firewall (adjust if not using UFW):
   ```bash
   sudo ufw allow 27015/tcp
   sudo ufw allow 34197/udp
   ```

## Usage

Clone this repository and run the following command:

```bash
docker compose up -d
```

This starts the Factorio server in detached mode. You can view the logs with:

```bash
docker compose -f path/to/docker-compose.yaml logs -f
```


## Further Customization

- Edit `RCON_PASSWORD` to secure remote control access.
- If you want to use mods or existing Factorio saves, place them in the `data` folder.
- For more advanced configurations, check out the official [Factoriotools/Factorio Docker repository](https://github.com/factoriotools/factorio-docker).
