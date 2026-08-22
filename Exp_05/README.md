# EXPERIMENT 05 - CLOUDSIM

---

## AIM

To simulate a **cloud scenario using CloudSim** and run a scheduling algorithm that is not present in CloudSim.

---

## SOFTWARE REQUIRED

* Eclipse IDE
* CloudSim 3.0.3
* Apache Commons Math 3.6.1
* Java
* Windows 64-bit Operating System

---

## PROCEDURE

### 1. Download Eclipse

1. Download **Eclipse IDE for Java Developers**.
2. Select the appropriate version for a **Windows 64-bit** system.
3. Extract the downloaded Eclipse package.
4. Open `Eclipse.exe`.

---

### 2. Download CloudSim

Download **CloudSim 3.0.3** from the GitHub repository.

```text
CloudSim 3.0.3
```

Extract the downloaded CloudSim project files.

---

### 3. Download Apache Commons Math

Download **Apache Commons Math 3.6.1**.

Extract the downloaded package.

The required JAR file is:

```text
commons-math3-3.x.jar
```

---

### 4. Create CloudSim Project in Eclipse

1. Open **Eclipse**.
2. Navigate to:

```text
File → New → Project
```

3. Select **Java Project**.
4. Click **Next**.
5. Enter the project name:

```text
CloudSim
```

6. Unselect **Use default location**.
7. Browse to the location where the CloudSim source code was extracted.
8. Click **Next**.

---

### 5. Configure CloudSim Libraries

1. Open the **Libraries** tab.
2. Check whether `commons-math3-3.x.jar` is already available.
3. If it is not available, click **Add External JARs**.
4. Navigate to the extracted Apache Commons Math directory.
5. Select:

```text
commons-math3-3.x.jar
```

6. Click **Open**.
7. Verify that the external JAR appears in the library list.
8. Click **Finish**.

Eclipse will configure and build the CloudSim project.

---

### 6. Open CloudSim Example

1. Open **Project Explorer**.
2. Navigate to the `examples` folder.
3. Expand:

```text
org.cloudbus.cloudsim.examples
```

4. Open:

```text
CloudsimExample1.java
```

---

### 7. Run the CloudSim Simulation

Run the program using:

```text
Run → Run
```

or use the keyboard shortcut:

```text
Ctrl + F11
```

The simulation output will be displayed in the Eclipse console.

---

## PROJECT STRUCTURE

```text
CloudSim/
│
├── bin/
├── docs/
├── examples/
│   └── org.cloudbus.cloudsim.examples/
│       └── CloudsimExample1.java
├── src/
└── libraries/
    └── commons-math3-3.x.jar
```

---

## WORKFLOW

```text
Download Eclipse
        │
        ▼
Download CloudSim
        │
        ▼
Download Apache Commons Math
        │
        ▼
Create Java Project
        │
        ▼
Configure CloudSim Source
        │
        ▼
Add External JAR
        │
        ▼
Build CloudSim Project
        │
        ▼
Open CloudsimExample1.java
        │
        ▼
Run Simulation
        │
        ▼
View Output in Console
```

---

## EXPECTED OUTPUT

After successful execution, the CloudSim simulation output should be displayed in the **Eclipse Console**.

The experiment verifies that the CloudSim environment has been configured and the example simulation executes successfully.

---

## RESULT

Thus, the **cloud scenario was simulated successfully using the CloudSim framework in the Eclipse environment.**

---
