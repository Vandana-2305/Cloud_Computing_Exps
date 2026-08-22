# EXPERIMENT 02 - VIRTUAL MACHINE – C COMPILER

---

## AIM

To install a **C compiler** in the Virtual Machine created using VirtualBox and execute simple C programs.

---

## SOFTWARE REQUIRED

* VMware Player / VirtualBox
* Virtual Machine
* CorePlus Guest Operating System
* C Compiler
* GCC
* Terminal

---

## PROCEDURE

### 1. Install VMware Player

Install the **VMware Player** and host the Virtual Machine using the CorePlus operating system.

### 2. Start the Virtual Machine

1. Open the VMware Workstation.
2. Power on the Virtual Machine.
3. Wait for the Guest Operating System to load.

### 3. Install the C Compiler

Open the terminal inside the Guest Operating System and execute:

```bash
tce-load -wi compiletc
```

The required libraries and GCC compiler will be downloaded and installed.

### 4. Create a C Program

Open the terminal and use the editor:

```bash
sudo editor
```

Enter the C program and save the file with the `.c` extension.

### 5. Exit the Editor

After completing the program, exit the editor using:

```text
CTRL + Q
```

The control will return to the terminal.

### 6. Compile the C Program

Compile the program using:

```bash
cc filename.c
```

Example:

```bash
cc demo.c
```

### 7. Execute the Program

Run the compiled program using:

```bash
./a.out
```

Example:

```text
Enter year: 1991
1991 is not a Leap Year
```

---

## COMMANDS USED

```bash
tce-load -wi compiletc

sudo editor

cc demo.c

./a.out
```

---

## WORKFLOW

```text
Start Virtual Machine
        │
        ▼
Open Terminal
        │
        ▼
Install C Compiler
        │
        ▼
Create C Program
        │
        ▼
Save as .c File
        │
        ▼
Compile using cc
        │
        ▼
Execute using ./a.out
        │
        ▼
Display Output
```

---

## EXPECTED OUTPUT

The C program should compile successfully and produce the expected output in the terminal.

Example:

```text
Enter year: 1991
1991 is not a Leap Year
```

---

## RESULT

Thus, the **C compiler was successfully installed in the Virtual Machine and simple C programs were compiled and executed successfully.**

---

## EXPERIMENT DETAILS

| Property                | Details                      |
| ----------------------- | ---------------------------- |
| **Experiment No.**      | 02                           |
| **Experiment Name**     | Virtual Machine – C Compiler |
| **Virtualization**      | VMware / VirtualBox          |
| **Guest OS**            | CorePlus                     |
| **Compiler**            | GCC / C Compiler             |
| **Compilation Command** | `cc filename.c`              |
| **Execution Command**   | `./a.out`                    |
| **Status**              | Completed                    |

---
