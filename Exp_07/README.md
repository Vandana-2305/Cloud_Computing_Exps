# EXPERIMENT 07 - HADOOP SINGLE NODE CLUSTER

---

## AIM

To install and configure a **Hadoop Single Node Cluster** and run simple applications such as **WordCount**.

---

## INTRODUCTION

**Apache Hadoop** is an open-source software framework used for storage and large-scale processing of datasets on clusters of commodity hardware.

The Hadoop framework consists of the following major modules:

* **Hadoop Common** - Libraries and utilities required by other Hadoop modules.
* **HDFS** - Hadoop Distributed File System for storing data.
* **YARN** - Resource-management platform for managing computing resources.
* **MapReduce** - Programming model for large-scale data processing.

---

## SOFTWARE REQUIRED

* Ubuntu / Linux Operating System
* Java
* OpenJDK
* SSH Server
* Apache Hadoop
* Terminal
* Hadoop 2.7.0

---

## PROCEDURE

### 1. Install Java

Java is required as a prerequisite for Hadoop.

Update the package repository:

```bash
sudo apt-get update
```

Install Java:

```bash
sudo apt-get install openjdk-7-jdk
sudo apt-get install openjdk-7-jre
```

Verify the Java installation:

```bash
java -version
```

The manual uses Java 1.7 for this experiment.

---

### 2. Install SSH Server

Install the OpenSSH server:

```bash
apt-get install openssh-server
```

SSH is required for communication with the local Hadoop node.

---

### 3. Generate SSH Key

Generate an RSA key:

```bash
ssh-keygen -t rsa -P "" -f ~/.ssh/id_rsa
```

Add the public key to the authorized keys:

```bash
cat $HOME/.ssh/id_rsa.pub >> $HOME/.ssh/authorized_keys
```

This allows the master node to act as a local slave without requiring a password.

---

### 4. Create Hadoop User and Group

Create the Hadoop group:

```bash
sudo addgroup hadoop
```

Create the Hadoop user:

```bash
sudo adduser --ingroup hadoop hadoop
```

---

### 5. Extract Hadoop

Copy the Hadoop archive to the home directory.

Extract Hadoop:

```bash
sudo tar -xzvf hadoop-2.7.0.tar.gz -C /usr/local/lib/
```

Change the ownership:

```bash
sudo chown -R hadoop:hadoop /usr/local/lib/hadoop-2.7.0
```

---

### 6. Create HDFS Directories

Create the NameNode directory:

```bash
sudo mkdir -p /var/lib/hadoop/hdfs/namenode
```

Create the DataNode directory:

```bash
sudo mkdir -p /var/lib/hadoop/hdfs/datanode
```

Change ownership:

```bash
sudo chown -R hadoop /var/lib/hadoop
```

---

### 7. Configure Environment Variables

Find the Java installation path:

```bash
readlink -f /usr/bin/java
```

Edit `.bashrc` and configure the Hadoop environment variables.

```bash
export JAVA_HOME=/usr/lib/jvm/java-7-openjdk-amd64
export HADOOP_INSTALL=/usr/local/lib/hadoop-2.7.0
export PATH=$PATH:$HADOOP_INSTALL/bin
export PATH=$PATH:$HADOOP_INSTALL/sbin
export HADOOP_MAPRED_HOME=$HADOOP_INSTALL
export HADOOP_COMMON_HOME=$HADOOP_INSTALL
export HADOOP_HDFS_HOME=$HADOOP_INSTALL
export YARN_HOME=$HADOOP_INSTALL
```

Reload the configuration:

```bash
source ~/.bashrc
```

The manual also configures additional Hadoop library and native library environment variables.

---

## HADOOP CONFIGURATION

### 8. Configure `hadoop-env.sh`

Open:

```text
/usr/local/lib/hadoop-2.7.0/etc/hadoop/hadoop-env.sh
```

Set:

```bash
export JAVA_HOME=/usr/lib/jvm/java-7-openjdk-amd64
```

---

### 9. Configure `core-site.xml`

Edit:

```text
core-site.xml
```

Configuration:

```xml
<configuration>
    <property>
        <name>fs.default.name</name>
        <value>hdfs://localhost:9000</value>
    </property>
</configuration>
```

---

### 10. Configure `yarn-site.xml`

Edit:

```text
yarn-site.xml
```

Add:

```xml
<configuration>
    <property>
        <name>yarn.nodemanager.aux-services</name>
        <value>mapreduce_shuffle</value>
    </property>

    <property>
        <name>yarn.nodemanager.aux-services.mapreduce.shuffle.class</name>
        <value>org.apache.hadoop.mapred.ShuffleHandler</value>
    </property>
</configuration>
```

---

### 11. Configure `mapred-site.xml`

Create the configuration file from the template:

```bash
cp mapred-site.xml.template mapred-site.xml
```

Configure MapReduce to use YARN:

```xml
<configuration>
    <property>
        <name>mapreduce.framework.name</name>
        <value>yarn</value>
    </property>
</configuration>
```

---

### 12. Configure `hdfs-site.xml`

Configure the replication factor and HDFS storage directories:

```xml
<configuration>
    <property>
        <name>dfs.replication</name>
        <value>1</value>
    </property>

    <property>
        <name>dfs.namenode.name.dir</name>
        <value>file:/var/lib/hadoop/hdfs/namenode</value>
    </property>

    <property>
        <name>dfs.datanode.data.dir</name>
        <value>file:/var/lib/hadoop/hdfs/datanode</value>
    </property>
</configuration>
```

These settings correspond to the single-node configuration described in the manual.

---

## HADOOP ARCHITECTURE

```text
                 HADOOP
                    │
        ┌───────────┼───────────┐
        │           │           │
        ▼           ▼           ▼
 Hadoop Common     HDFS        YARN
                    │           │
                    │           ▼
                    │      Resource
                    │      Management
                    │
                    ▼
              Data Storage
                    │
                    ▼
               MapReduce
                    │
                    ▼
             Data Processing
```

---

## WORKFLOW

```text
Install Java
     │
     ▼
Install SSH
     │
     ▼
Generate SSH Key
     │
     ▼
Create Hadoop User
     │
     ▼
Install Hadoop
     │
     ▼
Create HDFS Directories
     │
     ▼
Configure Environment
     │
     ▼
Configure Hadoop XML Files
     │
     ▼
Start Hadoop Services
     │
     ▼
Run Hadoop Applications
     │
     ▼
WordCount / Simple Application
```

---

## EXPECTED OUTPUT

The Hadoop Single Node Cluster should be configured successfully and Hadoop applications such as **WordCount** should execute successfully.

---

## RESULT

Thus, the **Hadoop Single Node Cluster was successfully installed and configured, and simple Hadoop applications such as WordCount were executed.**

---

