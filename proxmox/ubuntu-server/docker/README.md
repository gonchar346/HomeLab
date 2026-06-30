# Docker

## Overview

Docker is installed on the Ubuntu Server virtual machine and is used as the container platform for the HomeLab environment.

All infrastructure services running on this VM will be deployed as Docker containers.

---

## Purpose

Docker is used to:

- simplify service deployment;
- isolate applications;
- make services reproducible;
- manage infrastructure with Docker Compose.

---

## Installed Components

The following components are installed:

- Docker CE
- Docker CLI
- containerd
- Docker Buildx
- Docker Compose Plugin

---

## Installation

Docker was installed from the official Docker repository.

The Docker GPG key and repository were added manually.

The user `alexey` is a member of the `docker` group, allowing Docker commands to be executed without `sudo`.

---

## Verification

Docker version:

```bash
docker --version
```

Docker Compose version:

```bash
docker compose version
```

Running containers:

```bash
docker ps
```

Downloaded images:

```bash
docker images
```

---

## Project Structure

```text
docker/
├── README.md
└── nginx/
    ├── README.md
    ├── compose.yml
    └── html/
        └── index.html
```

Additional services will be added here as the lab grows.

---

## Current Services

| Service | Status |
|----------|--------|
| Nginx | ✅ Running |

---

## Learning Objectives

Current topics:

- Docker Images
- Docker Containers
- Docker Compose
- YAML
- Port Mapping
- Bind Mounts

Future topics:

- Docker Networks
- Docker Volumes
- Multi-container Applications
- Reverse Proxy
- Docker Logs
- Docker Health Checks

---

## Notes

Docker services in this repository represent the actual configuration used in the HomeLab environment.

Every new service will have its own directory containing:

- README.md
- compose.yml
- configuration files
- application data (when applicable)