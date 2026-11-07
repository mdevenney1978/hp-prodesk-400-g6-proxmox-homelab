Proxmox VE – Network Configuration

Overview

This document will record the network configuration of the HP ProDesk 400 G6 Mini running Proxmox VE.

The objective is to develop practical experience with network interfaces, IP addressing, virtual networking, Linux bridges and network segmentation.

Network Objectives

* Configure reliable network connectivity for the Proxmox host.
* Understand Proxmox virtual network bridges.
* Connect virtual machines to appropriate networks.
* Explore network segmentation and isolation.
* Develop practical networking and troubleshooting skills.
* Build a controlled environment for cybersecurity testing.

Physical Network Configuration

The physical network configuration will be documented during installation.

Component	Details
Host	HP ProDesk 400 G6 Mini
Network connection	To be confirmed
Physical interface	To be confirmed
IP address	To be configured
Gateway	To be configured
DNS	To be configured

Proxmox Virtual Networking

Proxmox networking will be configured and documented after installation.

Topics to explore:

* Linux network bridges.
* Virtual machine network interfaces.
* Static and dynamic IP addressing.
* DHCP and DNS.
* Network isolation.
* VLANs and network segmentation.

Planned Network Architecture

The initial network design will prioritise reliable management access and controlled connectivity for virtual machines.

Further network segmentation and isolated cybersecurity testing environments will be introduced as the lab develops.

Security Considerations

* Keep management access restricted to trusted devices.
* Avoid exposing the Proxmox management interface directly to the internet.
* Use isolated networks for vulnerable test machines where appropriate.
* Document firewall and network access rules.
* Only test systems and networks owned by me or where explicit permission has been granted.

Network Diagrams

Network architecture diagrams will be added as the configuration develops.

Configuration Status

Status: Planned – Proxmox networking has not yet been configured.

This document will be updated as network interfaces, bridges, IP addressing and virtual machine connectivity are implemented and tested.