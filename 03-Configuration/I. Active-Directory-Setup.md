## 🗂️ Active Directory Configuration & Group Policy

This section covers creating Organizational Units, users, and groups, then configuring and verifying Group Policy Objects (GPOs) for Password Policy, Account Lockout Policy, and Desktop Wallpaper on the domain **Yeshi.local**.

---

### 👥 1. Organizational Units, Users & Groups

I created Organizational Units by department and populated them with users and security groups.

- **OUs Created:** IT, HR, Finance, Marketing, Sales
- **Example User:** John Smith (`jsmith@Yeshi.local`) — created in the IT OU
- **Example Groups:** IT-Staff (Global Security group), Sales-Staff (with member David Lee)
Yeshi.local
├── IT
├── HR
├── Finance
├── Marketing
└── Sales

📸 *New Object - User: Creating John Smith in the IT OU*

![New User Object](../06-Screenshots/IV.%20Active-Directory-Setup/2.png)

📸 *New Object - Group: Creating the IT-Staff Security Group*

![New Group Object](../06-Screenshots/IV.%20Active-Directory-Setup/3.png)

📸 *Sales-Staff Group Properties — Member David Lee*

![Sales-Staff Group Members](../06-Screenshots/IV.%20Active-Directory-Setup/4.png)

---

### 🔐 2. Password Policy Configuration

Configured the Default Domain Policy to enforce strong password requirements via Group Policy Management.

- **Enforce password history:** 10 passwords remembered
- **Maximum password age:** 90 days
- **Minimum password age:** 1 day
- **Minimum password length:** 10 characters
- **Password must meet complexity requirements:** Enabled

📸 *Group Policy Management Console — Forest: Yeshi.local*

![GPM Console](../06-Screenshots/IV.%20Active-Directory-Setup/9.png)

📸 *Group Policy Management — Expanded View (Domains, Sites, Modeling, Results)*

![GPM Expanded](../06-Screenshots/IV.%20Active-Directory-Setup/10.png)

📸 *Group Policy Management Editor — Password Policy (Before Configuration)*

![Password Policy Before](../06-Screenshots/IV.%20Active-Directory-Setup/11.png)

📸 *Maximum Password Age — Set to 90 Days*

![Maximum Password Age](../06-Screenshots/IV.%20Active-Directory-Setup/12.png)

📸 *Minimum Password Age — Set to 1 Day*

![Minimum Password Age](../06-Screenshots/IV.%20Active-Directory-Setup/13.png)

📸 *Minimum Password Length — Set to 10 Characters*

![Minimum Password Length](../06-Screenshots/IV.%20Active-Directory-Setup/14.png)

📸 *Password Must Meet Complexity Requirements — Enabled*

![Password Complexity](../06-Screenshots/IV.%20Active-Directory-Setup/15.png)

📸 *Enforce Password History — 10 Passwords Remembered*

![Password History](../06-Screenshots/IV.%20Active-Directory-Setup/17.png)

📸 *Password Policy — Final Configuration Summary*

![Password Policy Final](../06-Screenshots/IV.%20Active-Directory-Setup/18.png)

---

### 🚫 3. Account Lockout Policy

Configured account lockout settings to protect against brute-force login attempts.

- **Account lockout duration:** 30 minutes
- **Account lockout threshold:** 5 invalid logon attempts
- **Reset account lockout counter after:** 30 minutes

📸 *Account Lockout Policy — Final Configuration*

![Account Lockout Policy](../06-Screenshots/IV.%20Active-Directory-Setup/19.png)

---

### 🖼️ 4. Desktop Wallpaper Policy

Configured a GPO to enforce a standard desktop wallpaper across domain-joined machines.

📸 *Desktop Wallpaper Policy — Enabled*

![Desktop Wallpaper Policy](../06-Screenshots/IV.%20Active-Directory-Setup/20.png)

---

### 🧪 5. Verification

After configuring the GPOs, I verified policy application on **CLIENT01** using `whoami`, `gpupdate`, and `gpresult`.

📸 *Command Prompt — whoami Confirming Domain Login*

![whoami](../06-Screenshots/IV.%20Active-Directory-Setup/5.png)

📸 *gpupdate /force — Policy Update Completed Successfully*

![gpupdate](../06-Screenshots/IV.%20Active-Directory-Setup/21.png)

📸 *gpresult /r — RSOP Data for CLIENT01*

![gpresult Header](../06-Screenshots/IV.%20Active-Directory-Setup/6.png)

📸 *gpresult /r — Applied Group Policy Objects (Password Policy, Account Lockout Policy)*

![gpresult Applied GPOs](../06-Screenshots/IV.%20Active-Directory-Setup/22.png)

📸 *gpresult /r — Filtered GPOs and Computer Security Group Membership*

![gpresult Security Groups](../06-Screenshots/IV.%20Active-Directory-Setup/23.png)

📸 *gpresult /r — User Settings Showing Desktop Wallpaper Policy Applied*

![gpresult User Settings](../06-Screenshots/IV.%20Active-Directory-Setup/24.png)

📸 *Desktop Wallpaper Policy Applied on CLIENT01*

![Wallpaper Applied](../06-Screenshots/IV.%20Active-Directory-Setup/25.png)

---

### 📦 6. Summary

| GPO Name              | Setting                          | Value               |
|-----------------------|-----------------------------------|----------------------|
| Password Policy        | Enforce password history          | 10 passwords         |
| Password Policy        | Maximum password age              | 90 days               |
| Password Policy        | Minimum password age              | 1 day                  |
| Password Policy        | Minimum password length           | 10 characters         |
| Password Policy        | Password complexity requirements  | Enabled                |
| Account Lockout Policy | Account lockout duration          | 30 minutes            |
| Account Lockout Policy | Account lockout threshold         | 5 invalid attempts    |
| Account Lockout Policy | Reset lockout counter after       | 30 minutes            |
| Desktop Wallpaper Policy | Desktop Wallpaper                | Enabled                |

---

### 📁 7. Screenshot Storage

All screenshots for this section can be found in:
📂 [`06-Screenshots/IV. Active-Directory-Setup`](../06-Screenshots/IV.%20Active-Directory-Setup/)
