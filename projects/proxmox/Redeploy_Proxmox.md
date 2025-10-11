---
layout: default
title: Deploy Proxmox
parent: Proxmox
nav_order: 1
---

## Deploy Proxmox

I'll be deploying Proxmox VE 9.0 on my Home Lab server.

1. Download Proxmox ISO File to local Machine
2. Download Balena Etcher Software to Local Machine
3. Use Balena Etcher to write ISO data to USB Storage Device

## Installing and Configuration Proxmox
1. Boot up your Home Lab Server with USB Storage Device attached
2. Follow on Screen steps to install Proxmox software on M.2 Drive

Note:  
Once Proxmox software has been installed on M.2 Drive, take note of IP Address details. 

3. Remove USB Storage Device when Proxmox reboots.


From a Web Browser:  
1. Access Proxmox web console via IP Address details from above step.
2. 


```console
sudo apt-get update
```