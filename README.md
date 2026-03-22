# Containerization with Docker — Guide & Workspace Summary

**Overview**

This repository is a hands-on collection of Docker examples, reference commands, and small example apps to help you learn and apply containerization quickly. Contents are organized into focused folders so you can open only what you need. This README summarizes the repository so you don't have to open every folder.

**Quick Start**

- **Prerequisites:** Docker (Engine + CLI) installed and running. For compose examples, Docker Compose or Docker CLI v2 compose is required.
- **Common quick commands:**

      - Build an image from a Dockerfile:

      ```bash
      docker build -t my-image:latest -f "Common Docker commands/Dockerfile" .
      ```

      - Run a container (example):

      ```bash
      docker run --rm -p 8080:8080 my-image:latest
      ```

      - Start services with Compose (from a folder with `docker-compose.yaml`):

      ```bash
      docker compose up --build
      docker compose down
      ```

**Repository Structure (high level)**

- **Common Docker commands:** [Common Docker commands/README.md](Common%20Docker%20commands/README.md) — Short, curated command snippets and a simple Node.js example app. Useful files:
  - `docker_commands.md`: curated command list and examples
  - `Dockerfile`: example Dockerfile for the sample app
  - `docker-compose.yaml`: quick compose example

- **Container vs Image:** [Container vs Image /README.md](Container%20vs%20Image%20/README.md) — Notes and short how-tos demonstrating runtime vs image concepts, env vars, and verifying running containers.

- **Debug docker commands:** [Debug docker commands/README.md](Debug%20docker%20commands/README.md) — Troubleshooting commands (attach to running containers, shell into container, replace/manage containers) and step-by-step tips.

- **Deploy docker application on a server:** [Deploy docker application on a server/README.md](Deploy%20docker%20application%20on%20a%20server/README.md) — Example compose deployments, ECR/docker registry notes, and commands you can run on a remote host.

- **Deploy Nexus as Docker Container:** [Deploy Nexus as Docker Container/README.md](Deploy%20Nexus%20as%20Docker%20Container/README.md) — Steps to provision a droplet and run Nexus as a container (useful if you host Docker images in Nexus).

- **Developing with Docker:** [Developing with Docker /README.md](Developing%20with%20Docker%20/README.md) — Step-by-step workflows for running MongoDB + mongo-express locally, creating networks, and integrating a node app.

- **Docker Compose - Run multiple Docker containers:** [Docker Compose - Run multiple Docker containers/README.md](Docker%20Compose%20-%20Run%20multiple%20Docker%20containers/README.md) — Compose automation and multi-container examples.

- **Docker Hosted Repository on Nexus:** [Docker Hosted Repository on Nexus/README.md](Docker%20Hosted%20Repository%20on%20Nexus/README.md) — Configure Docker daemon + authenticate with Nexus, push/pull image steps.

- **Docker Volumes - Persisting Data:** [Docker Volumes - Persisting Data/README.md](Docker%20Volumes%20-%20Persisting%20Data/README.md) — Examples demonstrating data persistence, mounting volumes and restarting containers safely.

- **Dockerfile - Build your own Docker Image:** [Dockerfile - Build your own Docker Image/README.md](Dockerfile%20-%20Build%20your%20own%20Docker%20Image/README.md) — A focused guide on building images from a Node.js app with step-by-step commands.


**What’s inside each example (quick notes)**

- **Sample Node.js apps**: Several folders include a tiny Node.js app and `server.js` + `package.json` (see `Deploy docker application on a server/app/` and `Dockerfile - Build your own Docker Image/app/`). These are minimal examples to illustrate containerizing a web app.

- **Compose examples**: Look for `docker-compose.yaml` in multiple folders. These show service definitions, ports, volumes, and networks used in different exercises.

- **Troubleshooting**: `Debug docker commands` collects commands you’ll use frequently (attach, logs, exec, docker ps, docker inspect).

**Common Scenarios & Copy-Paste Commands**

- Build & run the sample Node.js image (from repo root, adjust paths if needed):

```bash
# Build (uses example Dockerfile in the 'Common Docker commands' folder)
docker build -t sample-node:latest -f "Common Docker commands/Dockerfile" .

# Run the example app and map port 3000
docker run --rm -p 3000:3000 sample-node:latest
```

- Run the demo app with docker-compose (from a folder containing a `docker-compose.yaml`):

```bash
cd "Docker Volumes - Persisting Data" || exit
docker compose up --build
```

- Inspect a running container and open a shell inside it:

```bash
docker ps
docker logs <container-id>
docker exec -it <container-id> /bin/sh
```

**Tips & Best Practices**

- Use named volumes for persistent data (see `Docker Volumes - Persisting Data`).
- Keep small, focused Dockerfiles for examples — multi-stage builds are useful when you need smaller production images.
- For multi-container stacks, prefer `docker compose` and use `.env` files for secrets/ports where helpful.

**Where to start (suggested path for quick review)**

1. Read this file: [README.md](README.md)
2. Open [Common Docker commands/README.md](Common%20Docker%20commands/README.md) for quick curated commands and the example app.
3. If you want persistence examples, open [Docker Volumes - Persisting Data/README.md](Docker%20Volumes%20-%20Persisting%20Data/README.md).
4. If deploying to a server or using registries, check [Deploy docker application on a server/README.md](Deploy%20docker%20application%20on%20a%20server/README.md) and [Docker Hosted Repository on Nexus/README.md](Docker%20Hosted%20Repository%20on%20Nexus/README.md).

