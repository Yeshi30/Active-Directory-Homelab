# 🖥️ Windows Server 2022 Setup

This section documents the step-by-step process of installing and configuring **Windows Server 2022** as the Domain Controller (DC) for the lab environment. The process included setting a static IP, changing the computer name, installing Active Directory Domain Services, and promoting the server to a DC.

---

## 💾 1. Installation

- Created a new virtual machine in **VirtualBox** with the following specs:
  - **VM Name:** DC01
  - **RAM:** 2 GB
  - **CPU:** 2 cores
  - **Storage:** 50 GB
  - **Network:** Internal Network (intnet)
- Mounted the **Windows Server 2022 ISO** and completed the installation.
- Selected **Windows Server 2022 Datacenter Evaluation (Desktop Experience)** during setup.

📸 **Installation Setup Screen with Edition Selection**

![01](../06-Screenshots/II.%20Windows-Server-Setup/01.png)

---

## 💻 2. Initial Configuration

After installation, I performed the following:

- Changed the machine name to `DC01`
- Set a **static IP address:** `192.168.1.10`
- Configured DNS to point to itself (`192.168.1.10`)
- Set the time zone to **Australian Western Standard Time (UTC+08:00)**

📸 **System Info Showing DC01**

![04](../06-Screenshots/II.%20Windows-Server-Setup/04.png)

📸 **Network Settings Showing Static IP and DNS Config**

![05](../06-Screenshots/II.%20Windows-Server-Setup/05.png)

---

## 🧱 3. Installing AD DS Role

- Opened **Server Manager**
- Selected **Add Roles and Features**
- Installed the **Active Directory Domain Services (AD DS)** role
- Also installed **Group Policy Management** and **DNS Server**

📸 **AD DS Installation Progress**

![07](../06-Screenshots/II.%20Windows-Server-Setup/07.png)

---

## 🏰 4. Promoting to Domain Controller

- Promoted the server to a DC using the post-installation wizard
- Created a **new forest** named `Yeshi.local`
- Accepted the default NetBIOS name: `YESHI`
- Set the **DSRM password**
- Rebooted after setup completed

📸 **Deployment Configuration — New Forest Yeshi.local**

![09](../06-Screenshots/II.%20Windows-Server-Setup/09.png)

📸 **Domain Controller Options**

![10](../06-Screenshots/II.%20Windows-Server-Setup/10.png)

📸 **Prerequisites Check Passed**

![11](../06-Screenshots/II.%20Windows-Server-Setup/11.png)

---

## 🧪 5. Post-Installation Checks

- Logged in using the domain admin account
- Verified domain controller health using `dcdiag` in PowerShell
- Confirmed DNS was properly installed and functioning
- Verified `Yeshi.local` forward lookup zone in DNS Manager

📸 **dcdiag Results**

![12](../06-Screenshots/II.%20Windows-Server-Setup/12.png)

![13](../06-Screenshots/II.%20Windows-Server-Setup/13.png)

📸 **DNS Manager Showing Forward Lookup Zone for Yeshi.local**

![18](../06-Screenshots/II.%20Windows-Server-Setup/18.png)

---

## 📦 6. Summary

| Configuration Item | Value |
|---|---|
| **Server Name** | DC01 |
| **Static IP** | 192.168.1.10 |
| **Domain Name** | Yeshi.local |
| **DNS Server** | 192.168.1.10 (local) |
| **AD Role Installed** | Active Directory Domain Services |
| **Domain Controller Type** | New Forest |

---

## 📁 7. Screenshot Storage

All screenshots for this section can be found in:  
📂 [`06-Screenshots/II. Windows-Server-Setup`](../06-Screenshots/II.%20Windows-Server-Setup/)
