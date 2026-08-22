# EXPERIMENT 06 - FILE TRANSFER BETWEEN VIRTUAL MACHINES

---

## AIM

To find a procedure to **transfer files from one Virtual Machine to another Virtual Machine**.

---

## SOFTWARE REQUIRED

* Oracle VM VirtualBox
* Virtual Machines
* Guest Additions
* USB Drive
* Network Connection
* Host Operating System

---

## FILE TRANSFER METHODS

The following methods can be used to transfer files:

1. Copy and Paste
2. USB Drive
3. Network Share
4. Drag and Drop
5. Shared Folders

The lab manual specifically describes Copy and Paste, USB Drive, and Shared Folders in VirtualBox.

---

## PROCEDURE

### 1. Copy and Paste Data in VirtualBox

1. Start the Virtual Machine.
2. Open the VirtualBox menu.
3. Select:

```text
Devices → Drag and Drop
```

4. Select the required transfer mode:

* Host to Guest
* Guest to Host
* Bidirectional
* Disabled

5. Select **Bidirectional** for transferring files in both directions.

---

### 2. Transfer Files Using a USB Drive

1. Enable USB access in VirtualBox.
2. Install the **VirtualBox Extension Pack** if required.
3. Insert the USB device.
4. Open VirtualBox.
5. Navigate to:

```text
File → Preferences → Extensions
```

6. Click the **+** button.
7. Browse and select the downloaded Extension Pack.
8. Click **Open**.
9. Complete the installation.
10. Verify USB access under:

```text
Settings → USB
```

---

### 3. Create a Shared Folder

1. Install **VirtualBox Guest Additions** in the Guest OS.
2. Open:

```text
Devices → Install Guest Additions
```

3. Follow the installation wizard.
4. Restart the Guest OS if required.
5. Open:

```text
Devices → Shared Folders → Shared Folders Settings
```

6. Click the **+** button.
7. Select **Folder Path → Other**.
8. Browse and select the folder from the Host OS.
9. Enter a suitable shared-folder name.
10. Enable:

```text
Auto-mount
Make permanent
```

11. Click **OK**.

The selected folder can now be accessed from the Guest OS.

---

## WORKFLOW

```text
             FILE TRANSFER
                   │
        ┌──────────┼──────────┐
        │          │          │
        ▼          ▼          ▼
   Copy/Paste     USB     Shared Folder
        │          │          │
        ▼          ▼          ▼
   Host ↔ Guest  USB Device  Host ↔ Guest
```

---

## EXPECTED OUTPUT

Files should be successfully transferred between the Host/Guest or Virtual Machine environments using one of the available methods.

---

## RESULT

Thus, the **procedure to transfer files between Virtual Machines was successfully executed** using VirtualBox file-transfer methods.

---
