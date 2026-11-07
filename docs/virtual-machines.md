Proxmox VE – Virtual Machine Documentation

Overview

This document records the virtual machines (VMs) and containers deployed within the HP ProDesk 400 G6 Mini Proxmox cybersecurity homelab.

The aim is to gain practical experience in virtualisation, operating system administration, networking, infrastructure management and cybersecurity.

Virtual machines will be introduced progressively as hardware resources and project requirements allow.

Host Hardware

Component	Specification
System	HP ProDesk 400 G6 Mini
Processor	Intel Core i5-10500T
CPU	6 cores / 12 threads
Memory	8GB currently, 16GB planned
Primary storage	256GB NVMe SSD
Secondary storage	120GB Kingston SATA SSD
Hypervisor	Proxmox VE – planned

Planned Virtual Machines

1. Kali Linux

Purpose: Cybersecurity and penetration-testing learning.

Planned activities:

* Linux command-line administration.
* Network discovery and analysis.
* Vulnerability assessment.
* Security testing in authorised lab environments.
* Familiarisation with cybersecurity tools.

2. Ubuntu Server

Purpose: Linux server administration and infrastructure learning.

Planned activities:

* Linux administration.
* SSH configuration.
* User and permission management.
* Docker and containerisation.
* Server services and networking.

3. Windows

Purpose: Windows administration and security learning.

Planned activities:

* Windows installation and configuration.
* User and account management.
* System administration.
* Windows security settings.
* Troubleshooting and event log analysis.

4. Additional Security Testing Machines

Further virtual machines and vulnerable applications may be introduced as the lab develops.

These will provide controlled environments for learning vulnerability assessment, network security and defensive monitoring.

Virtual Machine Inventory

The following table will be updated as machines are deployed.

VM name	Operating system	Purpose	Status
Kali Linux	Kali Linux	Security testing	Planned
Ubuntu Server	Ubuntu Server	Linux administration	Planned
Windows	To be confirmed	Windows administration	Planned

Resource Allocation

CPU cores, RAM and virtual disk allocations will be recorded when each VM is created.

Resource allocation will take account of the host’s available memory and storage capacity.

The initial 16GB RAM configuration will require careful management when running multiple virtual machines simultaneously.

Containers

Proxmox containers (LXC) may also be used for lightweight Linux services and infrastructure applications.

Container deployments and configurations will be documented separately as they are introduced.

Testing and Results

Practical exercises, configuration changes, troubleshooting and learning outcomes will be recorded alongside each virtual machine.

Screenshots and supporting documentation will be added as the project progresses.

Current Status

Status: Planning – Proxmox VE has not yet been installed and no virtual machines have been deployed.

This document will be updated throughout the development of the homelab.