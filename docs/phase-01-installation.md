# Phase 01 — OPNsense Installation

## Objective

Install and prepare OPNsense 26.7 as the virtual firewall for the SOC lab.

## Virtual Machine Specifications

- VM Name: OPNsense-Firewall
- Guest OS: FreeBSD 14 64-bit
- Memory: 4000 MB
- CPU: 2 cores
- Virtual Disk: 20 GB SCSI
- VMware Workstation: 25H2

## Network Configuration

The OPNsense firewall VM was configured with three virtual network adapters:

| Adapter | VMware Network | Purpose |
|---|---|---|
| Network Adapter 1 | VMnet8 | WAN |
| Network Adapter 2 | VMnet9 | LAN |
| Network Adapter 3 | VMnet10 | DMZ |

## Installation

1. Created the OPNsense-Firewall virtual machine.
2. Allocated 4 GB RAM and 2 CPU cores.
3. Created a 20 GB virtual disk.
4. Configured three virtual network adapters.
5. Attached the official OPNsense 26.7 DVD ISO.
6. Booted the OPNsense installer.
7. Selected ZFS as the filesystem.
8. Selected Stripe (No Redundancy) because the lab uses a single virtual disk.
9. Installed OPNsense to the 20 GB virtual disk.
10. Rebooted the system from the installed virtual disk.

## Initial Verification

After installation, OPNsense successfully booted from:

`zroot/ROOT/default`

The OPNsense console was accessible using the root account.

The initial interface detection showed:

- LAN: em0
- WAN: em1
- Initial LAN IPv4: 192.168.1.1/24

The root password was reset successfully after installation before continuing with firewall configuration.

## Current Status

Phase 01 completed successfully.

### Next Phase

Phase 02 will configure:

- WAN interface
- LAN interface
- DMZ interface
- LAN IP: 192.168.200.1/24
- DMZ IP: 192.168.100.1/24
- WAN via DHCP

## Screenshots

- `screenshots/phase-01/01-opnsense-vm-settings.png`
- `screenshots/phase-01/02-vmware-network-editor.png`
- `screenshots/phase-01/07-opnsense-console-login.png`