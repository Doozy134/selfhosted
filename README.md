# Selfhosted - Docker Compose files

This repository contains a collection of folders, each with its own `docker-compose.yml` to deploy various self-hosted applications. Some folders also include an `example.env` 
as a template for passing in credentials / options to the docker compose file.


## Requirements

To get started with any of the applications, you need to have [Docker](https://www.docker.com/) and [Docker Compose](https://docs.docker.com/compose/) installed.

```bash
curl -sSL https://get.docker.com/ | CHANNEL=stable sh
systemctl enable --now docker
```
```bash
apt update
apt install docker-compose-plugin
```

## Folder Structure

Each folder in this repository corresponds to a different self-hosted application.


- `app1`, `app2`, `app3`, etc: Each folder relates to the specific application.
- `docker-compose.yml`: The Docker Compose file for the application.
- `example.env`: An example environment variables file. Copy this file to `.env` and fill in the necessary values.

## General Usage

Make a folder for the chosen app and change directory.

1. **Get docker-compose.yml for {folder}**

    ```bash
    curl https://raw.githubusercontent.com/Doozy134/selfhosted/main/{folder}/docker-compose.yml > docker-compose.yml
    # If there is an environment file
    curl https://raw.githubusercontent.com/Doozy134/selfhosted/main/{folder}/example.env > .env
    ```

2. **Edit the `.env` file** (if necessary) with your preferred text editor to configure environment variables.

3. **Start the application**

    ```bash
    docker-compose up -d
    ```
    
4. **Stop the application**

    To stop the application, run:

    ```bash
    docker-compose down
    ```
