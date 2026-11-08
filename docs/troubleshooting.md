Troubleshooting Log

1. Purpose

This document records technical issues encountered while building and maintaining the HP ProDesk 400 G6 Mini Proxmox homelab.

It will be updated as the project develops, documenting the symptoms, investigation, cause, resolution and verification of each issue.

The aim is to maintain a clear technical record and demonstrate practical troubleshooting and problem-solving skills.

2. Troubleshooting Process

When an issue occurs, the following process will be used:

1. Identify and describe the problem.
2. Record any error messages or unusual behaviour.
3. Investigate possible causes.
4. Carry out appropriate diagnostic checks.
5. Apply a suitable solution.
6. Test and verify that the issue has been resolved.
7. Record any lessons learned.

3. Hardware Troubleshooting

Potential areas for investigation include:

* RAM installation and detection.
* SSD detection and health.
* BIOS configuration.
* Cooling and temperature.
* Power and boot-related issues.
* Network adapter detection.

4. Proxmox Troubleshooting

Potential areas for investigation include:

* Installation and boot problems.
* Web interface access.
* Network bridge configuration.
* Storage configuration.
* Virtual machine creation and startup.
* Resource allocation and performance.
* Updates and package management.

5. Issue Log

Issue 1 — USB Installer Not Appearing in Rufus

Date: 8 November 2026

Component: Installation Media / USB

Problem description:

The 1TB USB drive was not initially visible in Rufus when preparing the Proxmox installation media.

Investigation:

Checked Rufus settings and enabled the option to display USB hard drives.

Identified cause:

Rufus was configured to hide USB hard drives by default.

Resolution:

Enabled the option to show USB hard drives, selected the Proxmox VE ISO and used DD Image mode when prompted.

Verification:

The installer USB was successfully created and used to boot the HP ProDesk.

Lessons learned:

Rufus may hide certain USB drives by default. Proxmox installation media can require DD Image mode.

⸻

Issue 2 — Proxmox Network Configuration

Date: 8 November 2026

Component: Networking / Proxmox

Problem description:

The Proxmox host required a correctly configured network connection to allow access to its web management interface.

Investigation:

Checked the laptop’s network configuration, including its IP address, subnet mask and default gateway. Confirmed the HP ProDesk was connected to the eero network using Ethernet.

Identified cause:

The Proxmox installation required appropriate management network settings.

Resolution:

Created an IP reservation in the eero router and configured the Proxmox management network.

Configuration:

* Hostname: pve01.homelab.local
* IP address: 192.168.5.186/22
* Gateway: 192.168.4.1
* DNS: 8.8.8.8

Verification:

The HP ProDesk appeared on the eero network and the Proxmox web interface was accessible.

Lessons learned:

Understanding IP addressing, subnet masks, gateways, DNS and DHCP reservations is important when configuring network infrastructure.

⸻

Issue 3 — Browser Security Warning

Date: 8 November 2026

Component: Proxmox / Networking

Problem description:

The browser displayed a security warning when accessing the Proxmox web management interface.

Investigation:

Identified that Proxmox uses a self-signed SSL certificate by default.

Identified cause:

The certificate was not issued by a certificate authority trusted by the browser.

Resolution:

Confirmed that this was expected behaviour on a new installation and proceeded to the local Proxmox management interface.

Verification:

Successfully accessed the Proxmox login page and logged in.

Lessons learned:

A browser certificate warning does not automatically indicate a security problem. It is important to understand why the warning appears before deciding how to proceed.

⸻

Issue 4 — Proxmox Subscription Notification

Date: 8 November 2026

Component: Proxmox

Problem description:

A notification appeared after logging into the Proxmox web interface stating that no valid subscription was available.

Investigation:

Identified the notification as the standard Proxmox subscription warning.

Identified cause:

The installation is using the free Proxmox VE edition without a paid subscription.

Resolution:

Dismissed the notification. Planned to configure the free No-Subscription repository.

Verification:

Successfully logged into the Proxmox management interface.

Lessons learned:

Proxmox VE can be used without a paid subscription for a personal homelab. Repository configuration is a separate task from subscription activation.