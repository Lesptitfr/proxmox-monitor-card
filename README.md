# Proxmox Monitor Card

A Home Assistant Lovelace card for monitoring Proxmox VE nodes, VMs/LXCs and optional Portainer services. The visual language is inspired by `juju35/ha-system-monitor-card`.

## V1

- Automatic discovery of Proxmox VE entities already exposed by Home Assistant
- Node, VM and LXC status
- CPU, RAM and storage gauges
- Uptime
- Network counters when available
- Optional Portainer services section
- Health/status and update indicators when available
- Responsive layout for phone and desktop
- No Proxmox or Portainer credentials stored in the card

## Installation with HACS

1. Open **HACS → Frontend**.
2. Open the three-dot menu → **Custom repositories**.
3. Add `https://github.com/Lesptitfr/proxmox-monitor-card`.
4. Select category **Dashboard**.
5. Install **Proxmox Monitor Card**.
6. Reload the browser resources if Home Assistant asks you to.

[![Open GitHub repository](https://img.shields.io/badge/GitHub-Lesptitfr%2Fproxmox--monitor--card-181717?logo=github)](https://github.com/Lesptitfr/proxmox-monitor-card)

## Lovelace

```yaml
type: custom:proxmox-monitor-card
title: Proxmox
show_host: true
show_services: true
show_network: true
show_storage: true
show_uptime: true
```

## Requirements

- Home Assistant Proxmox VE integration configured.
- Portainer integration configured if the Services section is desired.

## Roadmap

V2: hierarchical VM/LXC → Docker service grouping, better update information, disk I/O, temperatures, controls with confirmation, alert summaries and additional Proxmox storage details.
