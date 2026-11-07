HP ProDesk 400 G6 Mini – Storage Configuration

Overview

This document records the internal and external storage available for the Proxmox cybersecurity homelab.

The storage arrangement is designed to provide space for the Proxmox hypervisor, virtual machines, lab environments and backups.

Internal Storage

Primary Drive – NVMe SSD

* Capacity: 256GB
* Interface: NVMe
* Intended use: Proxmox VE installation and primary storage.

Secondary Drive – Kingston SSDNow 300

* Capacity: 120GB
* Form factor: 2.5-inch
* Interface: SATA
* Intended use: Additional virtual machine and lab storage.
* Installation: Fitted in the HP’s existing 2.5-inch drive caddy.

External Storage

External NVMe SSD

* Capacity: 512GB
* Connection: USB-C external enclosure.
* Intended use: Backup storage, transferring virtual machine images and project files.

Planned Storage Layout

Drive	Capacity	Purpose
Internal NVMe	256GB	Proxmox VE and primary storage
Internal SATA SSD	120GB	Additional lab storage
External NVMe	512GB	Backups and file transfers

Total internal capacity: 376GB

Future Considerations

Storage requirements will be reviewed as the homelab develops.

Potential future improvements include:

* Larger NVMe storage.
* Dedicated backup storage.
* Improved virtual machine storage allocation.

Current Status

The 256GB NVMe is installed in the system. The 120GB Kingston SATA SSD is fitted in the existing drive caddy.

Proxmox storage configuration has not yet been completed.
