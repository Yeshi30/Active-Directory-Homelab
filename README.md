# 🖥️ Active Directory Home Lab

## 📘 Overview

This repository documents my Active Directory home lab built using **VirtualBox** and **Windows Server 2022**. The lab simulates a small enterprise environment and covers domain setup, user management, Group Policy configuration, and client integration.

This project was built to develop practical IT support skills that directly map to entry-level helpdesk and sysadmin roles.

---

## 🏗️ Lab Architecture

![Lab Architecture](06-Screenshots/I.%20Planning/lab-architecture.png.png)

---

## 🛠️ Technologies Used

- **Virtualisation:** VirtualBox
- **Domain Controller OS:** Windows Server 2022 Datacenter Evaluation
- **Client OS:** Windows 10
- **Domain:** Yeshi.local
- **Tools:** Active Directory Users and Computers, Group Policy Management, DNS Manager, PowerShell

---

## 📂 Repository Structure

| Folder | Description |
|---|---|
| `01-Planning` | Lab objectives, architecture, and planning |
| `02-Environment-Setup` | VM setup for DC01 and CLIENT01 |
| `03-Configuration` | AD setup, GPO configuration, DNS |
| `04-Security-Policies` | Password and lockout policies |
| `06-Screenshots` | All lab screenshots organised by section |

---

## ✅ What Was Built

- ✅ Windows Server 2022 Domain Controller (DC01)
- ✅ Domain `Yeshi.local` with DNS
- ✅ Organisational Units — IT, HR, Finance, Marketing, Sales
- ✅ Domain users and security groups
- ✅ Windows 10 client (CLIENT01) joined to domain
- ✅ Group Policy Objects — Password Policy, Account Lockout Policy, Desktop Wallpaper
- ✅ GPO verified on CLIENT01 using `gpresult /r`

---

## 🎯 Skills Demonstrated

| Skill | Details |
|---|---|
| Windows Server Administration | Installed and configured Windows Server 2022 |
| Active Directory Management | OUs, users, groups, domain join |
| Group Policy | Password policy, lockout policy, wallpaper enforcement |
| Networking | Static IP, DNS, Internal Network configuration |
| Troubleshooting | dcdiag, gpresult, ping, nslookup |
| Documentation | GitHub markdown, structured technical writing |

---

## 📚 References

- [East Charmer – Windows Server Home Lab Project](https://www.youtube.com/@EastCharmer)
- [Active Directory Design and Planning Guide](https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/plan/ad-ds-design-and-planning)
- [Create Active Directory Test Environment](https://activedirectorypro.com/create-active-directory-test-environment/)
