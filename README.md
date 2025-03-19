# Excalidraw & Dungeon Revealer Deployment

This repository contains the Docker Compose configuration for deployment

## Getting Started

### Prerequisites
Before running this deployment, ensure you have:
- Docker installed ([Install Docker](https://docs.docker.com/get-docker/))
- Docker Compose installed ([Install Docker Compose](https://docs.docker.com/compose/install/))
- Git installed ([Install Git](https://git-scm.com/downloads))

### Clone This Repository
Clone this repository and navigate into the project directory:
```sh
git clone git@github.com:SD2-2024-Group-25/deployment.git
cd deployment
```

### Authenticate with GitHub Container Registry (GHCR)
Since the images are stored in GitHub Container Registry (GHCR), authentication is required before pulling them.

1. Generate a GitHub Personal Access Token (PAT) by going to [GitHub Tokens](https://github.com/settings/tokens) and selecting `write:packages` and `read:packages` scopes.
2. Log in to GHCR using the token:
```sh
echo YOUR_GITHUB_PAT | docker login ghcr.io -u YOUR_GITHUB_USERNAME --password-stdin
```

### Pull and Run Containers
Once authenticated, run the following commands to pull and start the containers:
```sh
docker-compose pull
docker-compose up -d
```
Use `docker ps` to verify that the containers are running.

### Accessing the Service
| Service | URL |
|---------|-----|
| Dungeon Revealer | [http://localhost:3000](http://localhost:3000) |

## Stopping the Deployment
To stop all containers:
```sh
docker-compose down
```
To remove all containers and volumes:
```sh
docker-compose down -v
```
