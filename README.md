# WSL Installation and Setup Guide

## Introduction

This guide documents my journey and the steps I followed to install and configure Windows Subsystem for Linux (WSL) on my Windows machine. WSL allows me to run a Linux environment directly within Windows, which is incredibly useful for development, testing, and learning Linux tools.

---

## Installation Steps

### **1. Enable WSL and Virtual Machine Platform**  *or check if your intel vt-x is enabled... mine is already enabled i checked it on Task Manager > Performance > Virtualization... and it says there "Enabled"*

To begin, I enabled the necessary Windows features by opening **PowerShell as Administrator** and running the following commands:

```
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

After running these commands, a system restart may be required.

---

### **2. Install the WSL Update Package**

I downloaded and installed the latest **WSL2 Linux kernel update package** from Microsoft's official documentation to ensure compatibility and performance improvements.

---

### **3. Set WSL 2 as the Default Version**

To ensure that all newly installed Linux distributions use WSL 2 by default, I ran:

```
wsl --set-default-version 2
```

---

### **4. Install a Linux Distribution (Ubuntu)**

I selected **Ubuntu** and downloaded it from the Microsoft Store. Upon launching it for the first time, I created my Linux username and password.

---

### **5. Initial Ubuntu Configuration**

After installing Ubuntu, I updated system packages and installed essential developer tools:

```
sudo apt update
sudo apt upgrade -y
sudo apt install build-essential git -y
```

---


*I was curious on how I can run linux on windows without using virtualbox/virtualmachine*

*I also downloaded kalilinux just tryout its tools*

