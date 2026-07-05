## 💻 Windows 10 Client Setup

This section details how I configured and joined a Windows 10 client—**CLIENT01**—to my domain **Yeshi.local**.

---

### 🖥️ 1. Virtual Machine Configuration

I created a new VM in VirtualBox with the following specifications:

- **VM Name:** CLIENT01
- **OS:** Windows 10
- **RAM:** 4 GB
- **CPU:** 2 cores
- **Disk:** 60 GB
- **Network Adapter:** Internal Network (same as Domain Controller)

📸 *Windows Setup — Installing Windows*

![Installing Windows](06-Screenshots/III-Windows-Client-Setup/01.png)

---

### 🌐 2. Network & Hostname Setup

After installation, I did the following on the client:

- Set the computer name to: `CLIENT01`
- Set a static IP address and DNS:
  - IP Address: `192.168.1.11`
  - Subnet Mask: `255.255.255.0`
  - Default Gateway: `192.168.1.1`
  - Preferred DNS Server: `192.168.1.10` (Domain Controller)
- Restarted the machine to apply changes

📸 *Device Specifications for CLIENT01 (Before Domain Join)*

![Device Specifications Before Domain Join](06-Screenshots/III-Windows-Client-Setup/02.png)

📸 *Network Settings with Static IP and DNS for CLIENT01*

![Static IP and DNS Configuration](06-Screenshots/III-Windows-Client-Setup/03.png)

---

### 🏢 3. Joining the Domain

On the client:

1. Opened **System Properties > Computer Name > Change**
2. Selected **Domain**, entered `Yeshi.local`
3. Supplied credentials for a domain admin account
4. Restarted the machine when prompted

📸 *Domain Join Prompt with Domain Name Entered*

![Domain Join Prompt](06-Screenshots/III-Windows-Client-Setup/04.png)

📸 *Confirmation Screen for Successful Domain Join*

![Confirmation Screen for Successful Domain Join](06-Screenshots/III-Windows-Client-Setup/04-.png)

---

### 🧪 4. Verification

After reboot, I:

- Logged in using domain credentials
- Verified domain membership in System Properties and the About page
- Confirmed connectivity to the Domain Controller via `ping` and `nslookup`
- Confirmed the client appeared in Active Directory Users and Computers

📸 *About Page Showing Domain-Joined Device (CLIENT01.Yeshi.local)*

![About Page Showing Domain Joined](06-Screenshots/III-Windows-Client-Setup/05.png)

📸 *System Properties Showing Domain Joined*

![System Properties Showing Domain Joined](06-Screenshots/III-Windows-Client-Setup/06.png)

📸 *Command Prompt Showing Successful Ping to Domain Controller*

![Ping to Domain Controller](06-Screenshots/III-Windows-Client-Setup/07.png)

📸 *Command Prompt Showing nslookup Resolving Yeshi.local*

![nslookup Yeshi.local](06-Screenshots/III-Windows-Client-Setup/08.png)

📸 *Active Directory Users and Computers Showing CLIENT01*

![ADUC Showing CLIENT01](06-Screenshots/III-Windows-Client-Setup/09.png)

---

### 📦 5. Summary

| Client Name | IP Address    | DNS Server    | Domain Joined |
|-------------|---------------|---------------|---------------|
| CLIENT01    | 192.168.1.11  | 192.168.1.10  | Yeshi.local   |

---

### 📁 6. Screenshot Storage

All screenshots for this section can be found in:
`06-Screenshots/III-Windows-Client-Setup`
