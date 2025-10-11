---
layout: default
title: Deploy Proxmox
parent: Proxmox
nav_order: 1
---

## Deploy Proxmox
Steps below will assist in setting up Proxmox on your Home Server


## Preparing the Installer 
1. Download the Proxmox ISO File to your local machine.
2. Download Balena Etcher to your local machine.
3. Use Balena Etcher to write the ISO data to a USB Storage Device.


## Installation and Initial Configuration
1. Boot up your Home Lab Server with the USB Storage Device attached.
2. Follow the on-screen steps to install Proxmox on the M.2 Drive.

    Note:  
    Once Proxmox has been installed on the M.2 Drive, be sure to make a note of the IP Address assigned to your server.

3. Remove the USB Storage Device when Proxmox reboots.


## Post-Install Setup (Web Console)
From a Web Browser on another computer:

1. Access the Proxmox web console by navigating to https://[Your-PVE-IP-Address]:8006/ (The connection must be secure-HTTPS).

2. Disable the Enterprise Repository: Navigate to Datacenter > Node > Updates > Repositories. Select the pve-enterprise repository and click Disable.

3. Add the No-Subscription Repository: Open the Shell Command Line from the web console and run the following command to add the community repository:
```
echo "deb [http://download.proxmox.com/debian/pve](http://download.proxmox.com/debian/pve) bookworm pve-no-subscription" > /etc/apt/sources.list.d/pve-no-subscription.list
```
4. Update and Upgrade: Use the following commands to get the latest software updates:
```
apt update && apt dist-upgrade -y
```
5. Reboot the Proxmox Server.  
