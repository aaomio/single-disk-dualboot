# Accessing and Attaching VHD in WinPE (Windows Setup)

This guide explains how to access the system drive, locate a VHD file, and attach it using DiskPart in Windows Preinstallation Environment (WinPE).

---

## 1. Boot into WinPE

Boot the system using a Windows installation USB:

- Press boot menu key (F12, F9, ESC depending on system)
- Select:
  UEFI: USB Device

Once Windows Setup loads:

Press:
Shift + F10

This opens Command Prompt (WinPE environment).

---

## 2. Identify system drive

In WinPE, drive letters may differ from normal Windows.

Try:
```cmd
C:
```

If Windows files are not found, try:
```cmd
D:
E:
F:
```

---

## 3. Locate VHD folder

Once on the correct drive, navigate to VHD location:
```cmd
cd VHD
dir /a
```

Verify the VHD file exists:
```cmd
Win10.vhdx
```

---

## 4. Open DiskPart

Run:
```cmd
diskpart
```
This launches the disk management CLI tool.

---

## 5. Select and attach VHD

Inside DiskPart:
```cmd
select vdisk file="C:\VHD\Win10.vhdx"
attach vdisk
```
This mounts the virtual hard disk so it becomes visible as a physical disk.

---

## 6. Verify attachment

Run:
```cmd
list volume
```
This should now list the VHD as a new volume.

---

## 7. Exit DiskPart
```cmd
exit
```
After exiting DiskPart:

- The tool closes
- The VHD remains ATTACHED
- It will appear as a normal disk/volume in Windows Setup or WinPE

---