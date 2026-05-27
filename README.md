# Windows VHD Dual Boot Setup (Documentation Repository)

This repository provides a structured workflow for installing Windows into a Virtual Hard Disk (VHDX) and configuring a dual-boot environment.

All steps must be followed in sequence.

---

## Workflow Overview

1. VHD creation
2. Create bootable USB (Rufus)
3. BIOS / UEFI preparation
4. Boot into WinPE
5. Attach VHD in WinPE
6. Install Windows into VHD
7. Boot configuration (dual boot)

---

## 1. VHD Creation (Core Step)

A Virtual Hard Disk (VHDX) is created as the first step in the process.

Reference:

- `vhd-setup/create-vhd.md`

Includes:

- DiskPart VHD creation
- Disk partitioning
- Disk formatting

---

## 2. Create Bootable USB (Rufus)

A bootable Windows installation USB is created.

Reference:

- `installation/windows-usb-rufus.md`

Includes:

- Windows ISO download
- Rufus configuration (GPT - UEFI)
- USB creation process

---

## 3. BIOS / UEFI Preparation

System firmware is configured in order to boot from the installation USB.

Reference:

- `installation/boot-from-usb.md`

Includes:

- Secure Boot configuration (if required)
- UEFI boot mode selection
- Boot menu access (F12 or system key)

---

## 4. Boot into WinPE

The system is booted from the USB installation media into Windows Setup.

Reference:

- `installation/windows-usb-boot-process.md`

Includes:

- Boot from USB
- Enter Windows Setup environment
- Open command prompt (Shift + F10)

---

## 5. Attach VHD in WinPE

After entering WinPE, the previously created VHD is attached.

Reference:

- `installation/vhd-winpe-attach.md`

Includes:

- Locating the VHD file
- Attaching via DiskPart
- Deploy Windows into the attached VHD using installation tools.


---

## 6. Boot Configuration (Dual Boot Setup)

Boot entries are configured to enable selection between operating systems.

Reference:

- `bcdedit/boot-configuration.md`

Includes:

- Boot entry creation
- Default OS selection
- Boot menu configuration
- Timeout settings

---

## Repository Structure
vhd-setup/
- create-vhd.md

installation/
- boot-from-usb.md
- windows-usb-rufus.md
- vhd-winpe-attach.md

bcdedit/
- boot-configuration.md