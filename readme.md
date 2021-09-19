# Theo's Podman Server Setup

This is a git repository that stores my podman + podman-compose server setup. It should also with docker and docker compose.

## Running With Podman

First, copy the example files and edit them to your liking.

```bash
# Caddy reverse proxy config
cp ./Caddyfile.example ./Caddyfile
# The .env file contains secret credentials that should not be exposed to the public
cp ./.env.example ./.env
```

```bash
git clone https://github.com/creepinson/podman-server-setup
cd podman-server-setup
sudo podman-compose up -d
```

## Running With Docker

First, you'll want to change the podman.sock to `/var/run/docker.sock` inside docker-compose.yml in order to get the drone ci runner to work.

Next, copy the example files and run the docker compose project.

```bash
# Caddy reverse proxy config
cp ./Caddyfile.example ./Caddyfile
# The .env file contains secret credentials that should not be exposed to the public
cp ./.env.example ./.env
```

```bash
git clone https://github.com/creepinson/podman-server-setup
cd podman-server-setup
# docker-compose if you are using the docker cli v1
docker compose up -d
```

## Services Included

- [Drone CI](https://www.drone.io/)
- [Gitea](https://gitea.io/)
- [Caddy reverse proxy with automatic ssl](https://caddyserver.com/)


