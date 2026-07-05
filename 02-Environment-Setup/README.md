# 🖥️ Environment Setup

## 📘 Overview

This section of the Active Directory Lab focuses on setting up the foundational environment required for deploying Active Directory services. It encompasses the installation and configuration of Windows Server and Windows Client operating systems within a virtualized environment, ensuring a controlled and isolated setup for testing and learning purposes.

---

## 🏗️ 1. Windows Server Setup

### 📝 Description

The initial step involves setting up a Windows Server machine that will later be configured as a Domain Controller. This server will host the Active Directory Domain Services (AD DS) and manage domain resources.

### 🛠️ Steps Performed

- **Installation of Windows Server:** Deployed Windows Server 2022 on a virtual machine using VirtualBox.
- **System Configuration:**
  - Assigned a static IP address (`192.168.1.10`) to ensure consistent network communication.
  - Changed the server hostname to `DC01` for easier identification.
  - Configured DNS to point to itself (`192.168.1.10`).
  - Set the time zone to Australian Western Standard Time (UTC+08:00).

Detailed instructions and configurations can be found in the `I. Windows-Server-Setup.md` file.

---

## 🖥️ 2. Windows Client Setup

### 📝 Description

Set up a Windows Client machine that will join the Active Directory domain. This client simulates a user workstation within the domain environment.

### 🛠️ Steps Performed

- **Installation of Windows Client OS:** Deployed Windows 10 on a virtual machine using VirtualBox.
- **System Configuration:**
  - Configured network settings to communicate with the Domain Controller.
  - Changed the client hostname to `CLIENT01`.
  - Set static IP address (`192.168.1.11`) and DNS pointing to DC01 (`192.168.1.10`).
  - Joined the machine to the `Yeshi.local` domain.

Detailed instructions and configurations can be found in the `II. Windows-Client-Setup.md` file.

---

## 📂 Files Included

- `I. Windows-Server-Setup.md` — Step-by-step guide for installing and configuring Windows Server 2022.
- `II. Windows-Client-Setup.md` — Instructions for setting up Windows 10 client and joining the domain.
- `README.md` — This documentation file summarizing the environment setup steps.

---

## ✅ Outcome

By completing these setup steps:

- **Prepared a Virtualised Environment:** Established isolated virtual machines for both server and client systems using VirtualBox.
- **Ensured Network Communication:** Configured Internal Network (intnet) to allow communication between DC01 and CLIENT01.
- **Laid the Foundation for Active Directory:** Set up the necessary infrastructure to proceed with AD installation and configuration.

---

## 📚 References

- [Building an Active Directory Home Lab](https://medium.com/@gwenilorac/empowering-your-learning-journey-building-an-active-directory-home-lab-807c436a7f04)
- [Create Active Directory Test Environment](https://activedirectorypro.com/create-active-directory-test-environment/)
- [East Charmer – Windows Server Home Lab Project](https://www.youtube.com/@EastCharmer)
