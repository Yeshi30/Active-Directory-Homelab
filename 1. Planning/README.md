🧭 ## Active Directory Lab – Planning Phase

📘 Overview

The planning phase is crucial for establishing a structured and efficient Active Directory (AD) lab environment. This phase involves defining the lab's objectives, designing the network topology, selecting appropriate hardware and software, and outlining the implementation roadmap. Proper planning ensures that the lab setup aligns with learning goals and simulates real-world IT support scenarios effectively.


🎯 Objectives


Skill Development: Gain hands-on experience with Active Directory services, including domain controllers, DNS, Group Policy Objects (GPOs), and user management.
IT Support Readiness: Build practical skills that directly map to entry-level IT support and helpdesk roles.
Testing Environment: Create a safe space to test configurations and security policies without affecting production systems.
Scenario Simulation: Replicate common enterprise environments to practice deployment, troubleshooting, and administrative tasks.



🗺️ Network Topology Design


Domain Structure: Single forest with one domain (Yeshi.local) to reflect a small-to-medium organisation.
Organisational Units (OUs): Designed OUs based on regions (USA, Asia, Europe) to manage policies and permissions effectively.
DNS: Configured on the Domain Controller to handle internal name resolution.
Client Integration: Windows 10/11 client machines joined to the domain to simulate end-user workstations.



🧰 Hardware and Software Requirements

Hardware

ComponentDetailsCPUIntel Core i5 or equivalentRAM16 GBStorageSSD with sufficient free space for VMs

Software

ComponentDetailsVirtualisation PlatformVirtualBoxDomain Controller OSWindows Server 2022 (Evaluation)Client OSWindows 10/11ISO FilesObtained from Microsoft Evaluation Center


📝 Implementation Roadmap


Environment Setup

Install and configure VirtualBox
Create virtual machines for server and client



Server Configuration

Install Windows Server 2022 on the DC VM
Assign static IP addresses and configure hostname



Active Directory Deployment

Promote server to Domain Controller
Configure DNS services
Create domain Yeshi.local



Client Configuration

Install Windows 10/11 on client VM
Join client machine to the domain



Group Policy Implementation

Create and link GPOs to OUs
Test policy application on client machines



User and Group Management

Create user accounts and security groups
Assign permissions and test access controls



Security Policies

Configure password and account lockout policies
Implement audit policies






📂 Files Included

Detailed documentation outlining the lab's objectives, network design, hardware/software requirements, and implementation steps can be found in:


Planning & Lab Overview.md
I. Windows-Server-Setup.md
II. Windows-Client-Setup.md
I. Active-Directory-Setup.md
II. DNS-Setup.md
III. GPO-Configurations.md
IV. Password-Policy.md
V. Account-Lockout-Policy.md



📚 References


Active Directory Design and Planning Guide
Create Active Directory Test Environment
East Charmer – Windows Server Home Lab Project
