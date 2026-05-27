# Windows Dual Boot Setup Using VHD

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
- [Create VHDX](vhd-setup/create-vhd.md)

Includes:
- DiskPart VHD creation
- Disk partitioning
- Disk formatting

---

## 2. Create Bootable USB (Rufus)

A bootable Windows installation USB is created.

Reference:
- [Windows USB (Rufus)](installation/windows-usb-rufus.md)

Includes:
- Windows ISO download
- Rufus configuration (GPT / UEFI)
- USB creation process

---

## 3. BIOS / UEFI Preparation

System firmware is configured in order to boot from the installation USB.

Reference:
- [BIOS / UEFI Boot Setup](installation/boot-from-usb.md)

Includes:
- Secure Boot configuration (if required)
- UEFI boot mode selection
- Boot menu access (F12 or system key)

---

## 4. Boot into WinPE and Attach VHD

The system is booted from the USB installation media into Windows Setup, and the VHD is then attached.

Reference:
- [VHD WinPE Attach](installation/vhd-winpe-attachvhd.md)

Includes:
- Boot from USB
- Enter Windows Setup environment
- Locate and attach VHD using DiskPart (Shift + F10)
- Prepare disk for Windows installation

---

## 5. Boot Configuration (Dual Boot Setup)

Boot entries are configured to enable selection between operating systems.

Reference:
- [BCDEdit Boot Configuration](bcdedit\boot-configuration.md)

Includes:
- Boot entry creation
- Default OS selection
- Boot menu configuration
- Timeout settings

---

## Repository Structure
\vhd-setup\
- create-vhd.md

\installation\
- boot-from-usb.md
- windows-usb-rufus.md
- vhd-winpe-attach.md

\bcdedit\
- boot-configuration.md