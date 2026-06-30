# Proxmox VE

## Purpose

Proxmox VE is used as the main hypervisor for the home lab.

It provides virtualization for Linux servers and future infrastructure services such as Docker, monitoring, automation and backup systems.

## Current Status

Proxmox VE is installed and operational.

The web interface is available and used for VM management, snapshots and hardware resource control.

## Implemented

- Installed Proxmox VE on physical hardware
- Configured basic management access
- Created Ubuntu Server virtual machine
- Enabled QEMU Guest Agent support for the VM
- Created VM snapshots for safe rollback

## Virtual Machines

### ubuntu-server

Purpose:

- Linux administration practice
- Docker host
- Future DevOps services

Installed system:

- Ubuntu Server 26.04 LTS
- SSH enabled
- Docker CE installed
- Docker Compose plugin installed
- QEMU Guest Agent installed

## Snapshots

Created snapshots:

- `clean_install`
- `updated`
- `ready_for_docker`

## Notes

Snapshots are used before major configuration changes.

They are not treated as backups. Their main purpose is fast rollback during lab experiments.