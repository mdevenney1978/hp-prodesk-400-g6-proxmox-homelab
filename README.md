# HP ProDesk 400 G6 Mini – Proxmox Cybersecurity Homelab

## Project Overview

This project documents the development of a dedicated IT infrastructure and cybersecurity homelab using an HP ProDesk 400 G6 Mini.

The objective is to build a practical virtualised learning environment using Proxmox VE, developing hands-on skills in server administration, virtualisation, networking, Linux, Windows administration and cybersecurity.

The project will document the complete process, from hardware preparation and Proxmox installation through to virtual machine deployment, network configuration and practical security exercises.

## Project Objectives

* Learn and deploy Proxmox VE.
* Develop practical virtualisation and server administration skills.
* Build and manage Windows and Linux virtual machines.
* Develop networking and infrastructure knowledge.
* Explore cybersecurity tools and techniques.
* Practise vulnerability assessment in controlled lab environments.
* Gain experience with Docker and containerisation.
* Document configurations, troubleshooting and learning outcomes.

## Hardware Specification

| Component | Specification |
|---|---|
| Manufacturer | HP |
| Model | ProDesk 400 G6 Mini |
| Processor | Intel Core i5-10500T |
| CPU | 6 cores / 12 threads |
| Installed RAM | 16GB DDR4-3200 (8GB original Samsung + 8GB Samsung M471A1K43DB1-CWE) |
| Primary storage | 256GB NVMe SSD |
| Secondary storage | 120GB Kingston SSDNow 300 SATA SSD |
| External storage | 512GB NVMe SSD in USB-C enclosure |

## Hardware Acquisition

The HP ProDesk 400 G6 Mini was purchased second-hand for £126.65, including postage.

The machine was supplied with a 256GB NVMe SSD and a Linux installation used by the seller for testing.

The original Samsung 8GB DDR4-3200 module was retained and a second Samsung 8GB DDR4-3200 SODIMM (M471A1K43DB1-CWE, PC4-25600S) was installed. The system now has 16GB of memory. See [RAM Upgrade](docs/ram-upgrade.md) for the installation and verification record.

A Kingston SSDNow 300 120GB SATA SSD is available for secondary internal storage and has been fitted in the existing 2.5-inch drive caddy.

## Planned Software and Technologies

* Proxmox VE – virtualisation platform.
* Kali Linux – penetration-testing and cybersecurity learning.
* Windows – operating system administration and security.
* Ubuntu Server – Linux and server administration.
* Docker – containerisation.
* Networking and monitoring tools.
* Vulnerable applications and controlled testing environments.

These technologies will be introduced progressively as the project develops.

## Planned Storage Configuration

| Drive | Intended purpose |
|---|---|
| 256GB NVMe | Primary Proxmox installation |
| 120GB SATA SSD | Additional VM and lab storage |
| 512GB external NVMe | Backup, transfer and project storage |

## Project Stages

### Stage 1 – Hardware Preparation

* [x] Acquire HP ProDesk 400 G6 Mini.
* [x] Identify Intel Core i5-10500T processor.
* [x] Confirm installed memory (16GB DDR4).
* [x] Confirm primary 256GB NVMe storage.
* [x] Identify existing 2.5-inch drive caddy.
* [x] Fit secondary 120GB SATA SSD.
* [x] Install additional 8GB RAM.
* [x] Verify final system memory.
* [ ] Check storage health.

### Stage 2 – BIOS and System Preparation

* [x] Inspect BIOS configuration.
* [ ] Verify Intel virtualisation settings (VT-x and VT-d).
* [x] Check boot configuration.
* [x] Prepare Proxmox installation USB.

### Stage 3 – Proxmox Installation and Configuration

* [x] Download Proxmox VE.
* [x] Create bootable USB installer using Rufus.
* [x] Install Proxmox VE onto the primary NVMe SSD.
* [x] Configure hostname and network settings.
* [x] Configure management IP address: 192.168.5.186.
* [x] Access the Proxmox web interface.
* [ ] Configure the free No-Subscription repository.
* [ ] Update Proxmox packages.
* [ ] Configure secondary SATA storage.

### Stage 4 – Virtual Machine Deployment

* [ ] Deploy Linux virtual machines.
* [ ] Deploy Windows virtual machines.
* [ ] Configure virtual networking.
* [ ] Explore Docker and containers.
* [ ] Test virtual machine backups and recovery.

### Stage 5 – Cybersecurity Learning

* [ ] Deploy controlled cybersecurity testing environments.
* [ ] Explore network monitoring.
* [ ] Practise vulnerability assessment.
* [ ] Configure and test security tools.
* [ ] Document practical exercises and learning outcomes.

### Stage 6 – Testing and Documentation

* [x] Document initial hardware configuration.
* [x] Document Proxmox installation.
* [ ] Capture further installation and configuration screenshots.
* [ ] Document network architecture.
* [ ] Record troubleshooting and solutions.
* [ ] Document practical learning outcomes.
* [ ] Update project documentation as the lab develops.

## Security and Responsible Use

All cybersecurity testing will be conducted within controlled environments using systems and networks owned by me or where explicit permission has been granted.

Network isolation and safe configuration will be considered when deploying vulnerable applications and testing environments.

## Project Status

**Current status:** Proxmox VE installed – initial configuration in progress. Hardware memory upgraded to 16GB and verified.

Proxmox VE has been successfully installed on the HP ProDesk 400 G6 Mini using the primary 256GB NVMe SSD. The management interface is accessible over the local network at 192.168.5.186:8006.

The 8GB-to-16GB RAM upgrade has been completed and verified. The next phase involves configuring the Proxmox repositories, applying system updates, verifying virtualisation settings and preparing the secondary 120GB SATA SSD for storage.

The project will continue to develop through the deployment of virtual machines, virtual networking and controlled cybersecurity testing environments.

This repository documents the practical setup, configuration decisions, screenshots, troubleshooting and learning outcomes throughout the project.

---

Personal IT infrastructure and cybersecurity learning project.
