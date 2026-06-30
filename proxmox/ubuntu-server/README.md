# Ubuntu Server VM

## Overview

This virtual machine is deployed inside Proxmox VE and is used as the main Linux server for the HomeLab environment.

The VM is currently used as a Docker host and will later be extended with additional infrastructure services.

---

## Role in HomeLab

```text
Proxmox VE
└── Ubuntu Server
    └── Docker
        └── Nginx
```

This VM is the first Linux server in the lab and acts as the foundation for containerized services.

---

## System Information

| Parameter      | Value                  |
| -------------- | ---------------------- |
| OS             | Ubuntu Server 26.04 LTS |
| Hostname       | ubuntu-server          |
| Virtualization | KVM                    |
| Hypervisor     | Proxmox VE             |
| Time Zone      | Europe/Moscow          |
| Management IP  | 192.168.10.24          |
| Main User      | alexey                 |

---

## Completed Configuration

- System packages updated
- SSH enabled and tested
- Remote access configured through MobaXterm
- QEMU Guest Agent installed
- QEMU Guest Agent enabled in Proxmox VE
- Time zone configured to `Europe/Moscow`
- Docker CE installed
- Docker Compose plugin installed
- User `alexey` added to the `docker` group
- First Docker Compose project deployed

---

## Access

The server is managed through SSH.

```bash
ssh alexey@192.168.10.24
```

MobaXterm is used as the main SSH client.

---

## QEMU Guest Agent

QEMU Guest Agent is installed inside the VM and enabled in Proxmox.

Check service status:

```bash
systemctl status qemu-guest-agent
```

Purpose:

- Better VM management from Proxmox
- Correct shutdown and reboot operations
- IP address visibility in Proxmox
- Improved integration between guest OS and hypervisor

---

## Docker

Docker is installed directly on this Ubuntu Server VM.

Installed components:

- Docker CE
- Docker CLI
- containerd
- Docker Buildx plugin
- Docker Compose plugin

Check versions:

```bash
docker --version
docker compose version
```

Docker services are stored under:

```text
proxmox/ubuntu-server/docker/
```

Current services:

```text
docker/
└── nginx/
```

---

## Snapshots

Proxmox snapshots were created during the initial setup process.

Current snapshots:

- `clean_install`
- `updated`
- `ready_for_docker`

Snapshots are used for quick rollback before major experiments.

They are not considered backups.

---

## Useful Commands

Check IP address:

```bash
hostname -I
```

Check SSH status:

```bash
systemctl status ssh
```

Check system information:

```bash
hostnamectl
```

Check time configuration:

```bash
timedatectl
```

Check Docker containers:

```bash
docker ps
```

Check Docker Compose services:

```bash
docker compose ps
```

---

## Notes

The Proxmox console is used only for initial setup or emergency access.

Normal administration is performed over SSH.