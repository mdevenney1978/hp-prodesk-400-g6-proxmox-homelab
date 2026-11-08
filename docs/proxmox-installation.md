Proxmox VE Installation – HP ProDesk 400 G6 Mini

Project: HP ProDesk 400 G6 – Proxmox Cybersecurity Homelab
Installation date: 8 November 2026
Status: Proxmox VE successfully installed

1. Overview

This document records the installation of Proxmox Virtual Environment (VE) on an HP ProDesk 400 G6 Mini.

The objective is to establish a dedicated virtualisation server that will eventually host virtual machines and containers for IT infrastructure, networking and cybersecurity learning.

The installation was completed using a bootable USB installer created with Rufus.

2. Hardware configuration

Component	Specification
Manufacturer	HP
Model	ProDesk 400 G6 Mini
Processor	Intel Core i5-10500T
Memory	16GB DDR4 RAM
Primary storage	256GB NVMe SSD
Secondary storage	120GB SATA SSD
Network	Integrated Ethernet

3. Installation preparation

The following steps were completed:

1. Downloaded the Proxmox VE installation ISO.
2. Downloaded and installed Rufus on a Windows 11 laptop.
3. Connected a 1TB external USB drive.
4. Selected the Proxmox ISO in Rufus.
5. Enabled USB hard drive visibility in Rufus.
6. Rufus identified the ISO as a hybrid image and enforced DD Image mode.
7. Created the bootable Proxmox installation media.

The USB drive was used solely as installation media.

4. BIOS and installation

The HP ProDesk was booted from the USB installation media using the HP startup boot menu.

The graphical Proxmox installer was selected.

The installation configuration was:

Setting	Configuration
Filesystem	ext4
Installation disk	256GB NVMe (/dev/nvme0n1)
Country	United Kingdom
Timezone	Europe/London
Keyboard layout	English (UK)
Administrator	root
Hostname entered	pve01.homelab.local

The 120GB SATA SSD was not selected as the installation target and is intended for secondary storage.

5. Network configuration

The home network uses an eero 6+ mesh system consisting of two units.

Initial network investigation identified the following configuration:

Setting	Value
Network gateway	192.168.4.1
Subnet mask	255.255.252.0
CIDR	/22
Proxmox IP address	192.168.5.186
Proxmox gateway	192.168.4.1
DNS server	8.8.8.8
Network interface	nic0
Connection	Wired Ethernet

The HP ProDesk was identified as a connected device in the eero application.

An IP reservation was created for 192.168.5.186 to maintain a consistent management address.

No port forwarding was configured. Proxmox management is intended to remain accessible through the local network.

6. First boot and management access

Following installation, the HP ProDesk successfully restarted and booted into Proxmox VE.

The server displayed its management address:

https://192.168.5.186:8006

The Proxmox web interface was subsequently accessed from a Windows 11 laptop.

Authentication was completed using the root administrator account and Linux PAM authentication.

A subscription notification was displayed because the installation does not have a paid Proxmox subscription.

This is expected when using the free installation.

7. Installation outcome

Successful installation milestones:

* Proxmox VE installed successfully.
* Installation completed on the NVMe drive.
* Wired network connectivity configured.
* Static management IP address configured and reserved.
* Proxmox successfully booted.
* Web management interface accessible.
* Root administrator login successful.

8. Outstanding configuration

The following tasks remain:

* Configure the free No-Subscription package repository.
* Refresh package lists and install available updates.
* Identify and configure the secondary 120GB SATA SSD.
* Review Proxmox storage configuration.
* Verify CPU virtualisation settings.
* Review system resources and memory allocation.
* Begin creating virtual machines and containers.

9. Learning outcomes

This installation provided practical experience in:

* Creating bootable Linux installation media.
* Understanding hybrid ISO images and DD image writing.
* Navigating BIOS and UEFI boot options.
* Installing a Type 1 hypervisor.
* Understanding static IP addressing and subnetting.
* Configuring network gateways and DNS.
* Creating DHCP reservations through an eero mesh router.
* Accessing and administering a virtualisation platform through a web interface.

10. Project status

The initial Proxmox installation milestone is complete.

The wider cybersecurity homelab project remains in development. Future stages will focus on virtualisation, storage management, network configuration and the deployment of isolated cybersecurity testing environments.

All testing will be conducted within authorised lab environments.