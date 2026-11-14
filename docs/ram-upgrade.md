# HP ProDesk 400 G6 Mini – RAM Upgrade

**Date completed:** 14 November 2026

## Overview

The system was upgraded from 8GB to 16GB of DDR4 memory by adding a second 8GB module while retaining the original memory.

The upgrade provides additional capacity for running multiple virtual machines and containers under Proxmox VE.

## Before the upgrade

- Installed memory: 8GB
- Original module: Samsung 8GB DDR4-3200
- Populated slot: DIMM1

## Installed configuration

| Memory slot | Manufacturer | Part number | Capacity | Specification |
|---|---|---|---:|---|
| DIMM1 | Samsung | Original module (part number not recorded) | 8GB | DDR4-3200 |
| DIMM3 | Samsung | M471A1K43DB1-CWE | 8GB | DDR4-3200 SODIMM, PC4-25600S |
| **Total** | | | **16GB** | **DDR4-3200** |

The original Samsung module was retained and a second Samsung 8GB DDR4-3200 SODIMM was installed in DIMM3. The added module is part number **M471A1K43DB1-CWE (PC4-25600S)**.

## Verification

The upgrade was checked in Proxmox/Linux using the following commands.

### Confirm installed memory modules

```bash
dmidecode -t 17
```

The output identified two memory devices, each reporting a capacity of 8192MB (8GB).

### Check recognised system memory

```bash
free -h
```

The system reported approximately 15GiB of usable memory. This is expected: Linux reports memory in GiB, and a small amount of installed physical memory may also be reserved for hardware.

The captured output showed approximately:

- Total memory: 15GiB
- Used memory: 1.7GiB
- Free memory: 13GiB
- Available memory: 13GiB
- Swap: 7.5GiB

Values are approximate and reflect the system state at the time of checking.

## Outcome

The memory upgrade was completed successfully. Both 8GB modules were detected, giving the HP ProDesk 400 G6 Mini 16GB of installed DDR4-3200 memory.

The additional capacity will support the next stages of the homelab build, including deploying and running multiple virtual machines and containers.

## Learning and documentation notes

This upgrade provided practical experience in:

- Identifying compatible desktop memory.
- Installing a memory module in a compact PC.
- Checking memory device information with `dmidecode`.
- Verifying operating-system memory recognition with `free`.
- Recording hardware changes and validation results.
