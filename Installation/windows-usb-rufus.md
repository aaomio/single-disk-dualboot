# Windows USB Creation Using Rufus

This document explains how to create a bootable Windows 10 USB using Rufus for use in a dual-boot / VHD setup.

---

## 1. Download Windows 10 ISO

Download the official Windows 10 ISO from Microsoft:

https://www.microsoft.com/software-download/windows10

You can use either:
- Media Creation Tool
- Direct ISO download

---

## 2. Download Rufus

Rufus is used to create a bootable USB installer.

https://rufus.ie

---

## 3. Prepare USB Drive

- Minimum 8GB USB recommended
- All data will be erased

---

## 4. Rufus Configuration

Open Rufus and set the following:

- Device: Your USB drive
- Boot selection: Windows 10 ISO
- Partition scheme: GPT
- Target system: UEFI (non-CSM)
- File system: NTFS
- Cluster size: Default

---

## 5. Create Bootable USB

Click:
Start → OK

Wait for process to complete.


