# Nginx

## Overview

This directory contains the first Docker Compose project deployed in the HomeLab environment.

The purpose of this service is to learn the Docker workflow, container lifecycle, port mapping and bind mounts.

---

## Project Structure

```text
nginx/
├── compose.yml
└── html/
    └── index.html
```

---

## Service Configuration

The service is deployed using Docker Compose.

Current configuration:

```yaml
services:
  nginx:
    image: nginx:latest
    ports:
      - "80:80"
    volumes:
      - ./html:/usr/share/nginx/html
```

---

## Components

### Image

```text
nginx:latest
```

Official Nginx image from Docker Hub.

### Port Mapping

```text
80:80
```

Host port **80** is forwarded to port **80** inside the container.

The service is accessible at:

```text
http://<server-ip>
```

Example:

```text
http://192.168.10.24
```

---

## Bind Mount

```text
./html:/usr/share/nginx/html
```

The local `html` directory is mounted into the container.

This allows editing the website without rebuilding or copying files into the container.

---

## Commands

Start:

```bash
docker compose up -d
```

Stop:

```bash
docker compose down
```

Restart:

```bash
docker compose restart
```

View running containers:

```bash
docker ps
```

View logs:

```bash
docker compose logs
```

---

## Learning Objectives

This project demonstrates:

- Docker Images
- Docker Containers
- Docker Compose
- YAML syntax
- Port Mapping
- Bind Mounts
- Basic container lifecycle management