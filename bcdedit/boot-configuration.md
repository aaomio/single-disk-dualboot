# Boot Configuration (BCDEdit) for Dual Boot / VHD

This guide explains how to configure Windows Boot Manager entries for dual boot using BCDEdit in Command Prompt.

---

## 1. View current boot entries
```cmd
bcdedit /enum
```
This shows all existing boot configurations including:
- Windows Boot Manager
- Installed OS entries

---

## 2. Create a new boot entry 

The correct way is to COPY an existing working entry:
```cmd
bcdedit /copy {default} /d "Windows VHD"
```
This returns a new GUID like: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}

---

## 3. Set boot entry as default (optional)
```cmd
bcdedit /default {GUID}
```
This makes the new entry the default OS.

---

## 4. Add entry to boot menu
```cmd
bcdedit /displayorder {GUID} /addlast
```
This ensures the entry appears in the boot menu.

---

## 5. Enable boot menu display
```cmd
bcdedit /set {bootmgr} displaybootmenu yes
```
This forces the boot menu to show.

---

## 6. Set timeout
```cmd
bcdedit /timeout 15
```
This sets boot menu timeout (seconds).

---

## 7. Verify configuration
```cmd
bcdedit /enum
```
Confirm:
- New entry exists
- Correct device and description
- Boot menu enabled

---

