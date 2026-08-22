# EXPERIMENT 01 - VIRTUAL WORKSTATION

---

## AIM

To install **VirtualBox / VMware / equivalent open-source cloud workstation** with different flavours of **Linux or Windows OS** on top of Windows 8 and above.

---

## SOFTWARE REQUIRED

* Oracle VM VirtualBox
* Windows Host Operating System
* Guest Operating System ISO Image
* Internet Connection

---

## PROCEDURE

### 1. Install VirtualBox

1. Open a web browser.
2. Visit the [VirtualBox website](https://www.virtualbox.org/wiki/Downloads).
3. Download the VirtualBox setup file.
4. Select **Windows Hosts** from the platform packages.

### 2. Run the Installation

1. Open the downloaded VirtualBox `.exe` file.
2. Click **Next** on the Welcome screen.
3. Choose the installation folder.
4. Select the required features.
5. Click **Next**.
6. Click **Yes** to install the Oracle VirtualBox network interfaces.
7. Click **Install**.
8. Wait for the installation to complete.
9. Click **Finish**.

### 3. Create a Virtual Machine

1. Open **Oracle VM VirtualBox**.
2. Click **New**.
3. Enter the following details:

| Setting               | Configuration                |
| --------------------- | ---------------------------- |
| **Name**              | Name of the Operating System |
| **Installation Path** | Default Path                 |
| **ISO Image**         | Guest OS ISO Image           |
| **Type**              | Linux / Windows / Mac        |
| **Version**           | Appropriate OS Version       |

### 4. Allocate Hardware Resources

Configure the resources for the Virtual Machine.

* **Base Memory:** 512 MB
* **Processors:** 1 CPU

Click **Next** after allocating the resources.

### 5. Create Virtual Hard Disk

1. Open the **Virtual Hard Disk Wizard**.
2. Allocate the required disk space.
3. Set the disk size to **2.00 GB**.
4. Click **Next**.
5. Review the Virtual Machine configuration.
6. Click **Finish**.

### 6. Start the Virtual Machine

1. Select the created Virtual Machine.
2. Click **Start**.
3. The Guest Operating System installation wizard will appear.
4. Follow the installation steps.
5. Complete the Guest OS installation.

### 7. Verify the Installation

After completing the installation, the Guest Operating System will boot successfully inside VirtualBox.

The experiment uses **Windows 98** as the Guest Operating System.

---

## CONFIGURATION

```text
Host OS        : Windows 10
Virtualization : Oracle VM VirtualBox
Guest OS       : Windows 98
Base Memory    : 512 MB
Processor      : 1 CPU
Disk Size      : 2.00 GB
```

---

## EXPECTED OUTPUT

The Virtual Machine should start successfully and display the installed Guest Operating System.

```text
Oracle VM VirtualBox
        │
        ▼
Virtual Machine
        │
        ▼
Windows 98 Guest OS
        │
        ▼
Windows 98 Desktop
```

---

## RESULT

Thus, **VirtualBox was installed successfully on the Windows host machine and Windows 98 was successfully installed as the Guest Operating System in the Virtual Machine.**

---

## EXPERIMENT DETAILS

| Property                    | Details              |
| --------------------------- | -------------------- |
| **Experiment No.**          | 01                   |
| **Experiment Name**         | Virtual Workstation  |
| **Virtualization Software** | Oracle VM VirtualBox |
| **Host OS**                 | Windows 10           |
| **Guest OS**                | Windows 98           |
| **Memory**                  | 512 MB               |
| **Processor**               | 1 CPU                |
| **Virtual Disk**            | 2.00 GB              |
| **Status**                  | Completed            |

---

The experiment procedure and configuration are based on the provided laboratory manual.
