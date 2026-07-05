# 🖥️ Windows Server 2022 Setup

This section documents the step-by-step process of installing and configuring **Windows Server 2022** as the Domain Controller (DC) for the lab environment.

---

## 💾 1. Installation

- **VM Name:** DC01
- **RAM:** 2 GB
- **CPU:** 2 cores
- **Storage:** 50 GB
- **Network:** Internal Network (intnet)
- Selected **Windows Server 2022 Datacenter Evaluation (Desktop Experience)**

📸 **OS Selection Screen**

![01](../06-Screenshots/I.%20Planning/06-Screenshots/II.%20Windows-Server-Setup/01.png.png)

📸 **Admin Password Setup**

![02](../06-Screenshots/II.%20Windows-Server-Setup/02.png)

📸 **First Boot — Server Manager Dashboard**

![03](../06-Screenshots/II.%20Windows-Server-Setup/03.png)

---

## 💻 2. Initial Configuration

- Changed machine name to `DC01`
- Set static IP: `192.168.1.10`
- DNS pointing to itself: `192.168.1.10`
- Time zone: Australian Western Standard Time (UTC+08:00)

📸 **System About Showing DC01**

![04](../06-Screenshots/II.%20Windows-Server-Setup/04.png)

📸 **Static IP and DNS Configuration**

![05](../06-Screenshots/II.%20Windows-Server-Setup/05.png)

---

## 🧱 3. Installing AD DS Role

- Opened Server Manager → Add Roles and Features
- Installed **Active Directory Domain Services**
- Also installed **Group Policy Management** and **DNS Server**

📸 **AD DS Installation Progress**

![06](../06-Screenshots/II.%20Windows-Server-Setup/06_png.png)

📸 **Server Manager Showing AD DS Role**

![07](../06-Screenshots/II.%20Windows-Server-Setup/07_png.png)

---

## 🏰 4. Promoting to Domain Controller

- Created a new forest named `Yeshi.local`
- NetBIOS name: `YESHI`
- Set DSRM password
- Rebooted after setup

📸 **Deployment Configuration — New Forest Yeshi.local**

![08](../06-Screenshots/II.%20Windows-Server-Setup/08_png.png)

📸 **Domain Controller Options**

![09](../06-Screenshots/II.%20Windows-Server-Setup/09_png.png)

📸 **Prerequisites Check Passed**

![10](../06-Screenshots/II.%20Windows-Server-Setup/10_png.png)

---

## 🧪 5. Post-Installation Checks

- Ran `dcdiag` to verify DC health
- Verified DNS forward lookup zone for `Yeshi.local`

📸 **dcdiag Results**

![11](../06-Screenshots/II.%20Windows-Server-Setup/11_png.png)

![12](../06-Screenshots/II.%20Windows-Server-Setup/12_png.png)

![13](../06-Screenshots/II.%20Windows-Server-Setup/13_png.png)

![14](../06-Screenshots/II.%20Windows-Server-Setup/14_png.png)

![15](../06-Screenshots/II.%20Windows-Server-Setup/15_png.png)

![16](../06-Screenshots/II.%20Windows-Server-Setup/16_png.png)

📸 **DNS Manager Showing Yeshi.local Forward Lookup Zone**

![17](../06-Screenshots/II.%20Windows-Server-Setup/17_png.png)

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
