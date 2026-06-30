# HomeLab

Personal infrastructure laboratory built on real hardware.

The goal of this project is to gain hands-on experience with enterprise networking, virtualization, Linux administration, infrastructure automation and DevOps practices.

---

## Hardware

| Device           | Model                      |
| ---------------- | -------------------------- |
| Router           | Cisco 2921                 |
| Switch           | Cisco Catalyst 2960-24TC-S |
| Internet Gateway | TP-Link Router             |
| Hypervisor       | Proxmox VE        |

---

## Network Design

| VLAN | Name       | Subnet          |
| ---- | ---------- | --------------- |
| 10   | Management | 192.168.10.0/24 |
| 20   | Users      | 192.168.20.0/24 |
| 30   | DMZ        | 192.168.30.0/24 |
| 50   | Servers    | 192.168.50.0/24 |

---

## Implemented

* Router-on-a-Stick
* Inter-VLAN Routing
* VLAN Segmentation
* DHCP
* NAT (PAT)
* SSH Management
* Trunk Links
* Access Ports
* Management VLAN
* Internet Connectivity
* Proxmox VE Deployment
* Ubuntu Server 26.04 LTS
* SSH Remote Management
* QEMU Guest Agent
* Docker CE
* Docker Compose
* First Docker Compose Project
* Nginx Container
* Bind Mounts

---

## Planned

* TrueNAS
* Ansible
* Zabbix
* WireGuard VPN
* GitHub Actions
* Automated Cisco Configuration Backups
* Portainer
* Gitea
* PostgreSQL
* Grafana
* Prometheus
* Traefik

---

## Current Status

The physical network is fully operational.

Completed:

* Cisco 2921 configured
* Cisco Catalyst 2960 configured
* VLAN segmentation operational
* Inter-VLAN routing operational
* DHCP operational
* NAT (PAT) operational
* SSH access enabled
* Internet connectivity verified
* Proxmox VE installed
* Ubuntu Server VM deployed
* QEMU Guest Agent enabled
* SSH configured for Ubuntu Server
* Docker CE installed
* Docker Compose installed
* First Docker Compose project deployed
* Nginx running in Docker
* Bind mount configured

---

## Repository Structure

```text
homelab/
├── README.md
├── CHANGELOG.md
├── .gitignore
│
├── docs/
│   ├── network/
│   ├── linux/
│   │   └── ubuntu-server.md
│   │
│   ├── docker/
│   │   ├── docker-basics.md
│   │   ├── yaml-notes.md
│   │   └── bind-mounts.md
│   │
│   └── notes/
│
├── cisco/
│
├── proxmox/
│   └── README.md
│
├── docker/
│   └── nginx/
│       ├── compose.yml
│       ├── README.md
│       └── html/
│           └── index.html
│
├── ansible/
└── scripts/
```

## Laboratory Topology



![HomeLab Topology](images/lab-topology.jpg)

## Project Goals

This repository documents the evolution of a real home lab built on enterprise hardware.

Every major configuration, topology change and service deployment is tracked using Git to document both the implementation process and infrastructure evolution.
