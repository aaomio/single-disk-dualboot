# BIOS / UEFI Setup for USB Boot

This guide explains how system firmware (BIOS / UEFI) is configured to allow booting from a Windows installation USB.

---

## 1. BIOS / UEFI Setup

BIOS/UEFI settings must be accessed during system startup.

Common keys:

- F2 (most laptops)
- DEL (most desktops)

---

## 2. Secure Boot

Secure Boot may need to be disabled depending on system requirements.

- Secure Boot: Disabled

---

## 3. Boot Mode

The system must be configured to use UEFI mode.

- UEFI mode (recommended)

Legacy/CSM should be disabled unless required.

---

## 4. Save and Exit

Changes must be saved before exiting BIOS/UEFI.

After restart:

- F12 is used to open the Boot Menu
- The USB installation device is selected