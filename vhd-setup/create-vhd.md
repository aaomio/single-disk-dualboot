# Create VHDX for Dual Boot

This guide explains how to create a Virtual Hard Disk (VHDX) for Windows dual boot.

---

## Step 1: Open DiskPart

Run in CMD:
```cmd
diskpart
```

---

## Step 2: Create VHD
```cmd
create vdisk file="C:\VHD\Win10.vhdx" maximum=20000 type=expandable
```

---

## Step 3: Select and attach
```cmd
select vdisk file="C:\VHD\Win10.vhdx"

attach vdisk
```

---

## Step 4: Create partition
```cmd
create partition primary

format quick fs=ntfs

assign letter=V

exit
```