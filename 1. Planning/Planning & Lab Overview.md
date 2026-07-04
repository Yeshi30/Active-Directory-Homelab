# 🧠 Planning & Lab Overview

---

## 📝 1. Objectives

The goal of this lab is to simulate a small enterprise Active Directory 
environment to build practical IT support skills. This lab is designed 
to mirror real-world helpdesk and sysadmin tasks expected in entry-level 
IT support roles.

Key focus areas include:

- Domain Controller deployment using **Windows Server 2022**
- Client machine domain joining with **Windows 10**
- Implementation of **Group Policy Objects (GPOs)** for security and user management
- Configuration of **DNS** and network services
- **User, group, and OU management** simulating a real company structure
- Troubleshooting and documenting common AD issues

---

## 🖼️ 2. Architecture Diagram

The diagram below illustrates the network structure, including the domain controller and client machine, and how they are logically connected.

📸 **Lab Architecture**

![Lab Architecture](../06-Screenshots/I.%20Planning/lab-architecture.png.png)

---

## 🛠️ 3. Lab Components

| Component | Details |
|---|---|
| **Domain** | Yeshi.local |
| **Domain Controller** | Windows Server 2022 (Evaluation) |
| **Client Machine** | Windows 10 |
| **Virtualisation** | VirtualBox |
| **Network Type** | Internal Network (VirtualBox) |
| **Host OS** | Windows 11 |

---

## ✅ 4. Pre-Requisites

- Host system with sufficient RAM
- VirtualBox installed
- Windows Server 2022 ISO (Microsoft Evaluation Center)
- Windows 10 ISO (Microsoft Media Creation Tool)
- Basic understanding of networking (IP, DNS)
- GitHub repository for documentation

---

## 🔍 5. Planning Considerations

- Used VirtualBox Internal Network for VM communication
- Domain name `Yeshi.local` for local enterprise simulation
- OUs organised by department (IT, HR, Finance, Marketing, Sales)
- Each step documented with screenshots
- Lab designed to support IT support job applications

---

## 📚 6. Skills Targeted

| Job Requirement | How This Lab Covers It |
|---|---|
| Windows environment experience | Windows Server 2022 administration |
| Identity management | AD users, groups, and OUs |
| Security tools exposure | GPO password and lockout policies |
| Troubleshooting skills | Documented issues and fixes |
| Networking fundamentals | DNS, static IP, domain communication |

---

## 📁 7. Screenshot Storage

All screenshots for this section can be found in:  
📂 [`06-Screenshots/I. Planning`](../06-Screenshots/I.%20Planning/)
