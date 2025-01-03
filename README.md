# 🌐 Active Directory Lab Repository

## Overview
This repository contains a step-by-step guide to building an **Active Directory Lab** using VirtualBox, Windows Server 2019, and Windows 10. Follow along to create a fully functional AD environment for hands-on learning in system administration and networking.

---

## 🛠️ Prerequisites
Before starting, ensure you have:
1. **VirtualBox** and its **Extension Pack** installed.
2. **ISO Files**:
   - [Windows Server 2019](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2019)
   - [Windows 10](https://www.microsoft.com/en-us/software-download/windows10ISO)
3. A computer with at least 8GB of RAM and sufficient storage.

---

## 📜 Walkthrough

### **Step 1: Install VirtualBox and Download ISOs**
- **[0:37]** Install VirtualBox and the Extension Pack:
  ![VirtualBox Installation](screenshots/step1-virtualbox.png)
- **[3:12]** Download the Windows Server 2019 and Windows 10 ISOs:
  ![Download ISOs](screenshots/step1-download-isos.png)

---

### **Step 2: Create the Domain Controller VM**
- **[4:42]** Create a new VM named `DC`:
  - Assign **2GB RAM**, and configure two network adapters:
    - NAT for internet.
    - Internal for the private network.
  ![Domain Controller Configuration](screenshots/step2-dc-configuration.png)

---

### **Step 3: Install Windows Server 2019**
- **[6:44]** Install Windows Server 2019:
  - Choose **Standard with Desktop Experience**.
  - Set the Administrator password to `Password1`.
  ![Server Installation](screenshots/step3-server-installation.png)

---

### **Step 4: Configure the Domain Controller**
- **[12:25]** Assign static IPs:
  - Internal NIC: `172.16.0.1`
  - Subnet Mask: `255.255.255.0`
  - DNS Server: `127.0.0.1`
  ![IP Configuration](screenshots/step4-ip-config.png)
- **[16:37]** Install Active Directory Domain Services (AD DS):
  ![AD DS Installation](screenshots/step4-adds-installation.png)

---

### **Step 5: Automate User Creation with PowerShell**
- **[31:38]** Download the PowerShell script and `names.txt`:
  - Add your name to the top of `names.txt`.
  ![Edit Names](screenshots/step5-edit-names.png)
- **[34:06]** Run the script to create 1,000 users:
  ![PowerShell Execution](screenshots/step5-powershell-execution.png)

---

### **Step 6: Create the Client VM**
- **[45:59]** Create a new VM named `Client1`:
  - Assign **4GB RAM** and an **Internal Network** adapter.
  ![Client VM Configuration](screenshots/step6-client-vm-config.png)

---

### **Step 7: Join the Client to the Domain**
- **[55:03]** Rename the client computer to `Client1` and join it to `mydomain.com`:
  ![Join Domain](screenshots/step7-join-domain.png)

---

### **Step 8: Verify Connectivity**
- **[54:13]** Check network connectivity:
  - Run `ipconfig` to confirm the client received an IP from DHCP.
  ![IP Configuration Verification](screenshots/step8-ip-verification.png)
- **[59:08]** Log in to the client using a domain account.
  ![Domain Login](screenshots/step8-domain-login.png)

---

## 🎯 Features
1. **Active Directory Management:** Centralized user and group management.
2. **Networking Services:** Configured DNS, DHCP, and NAT for seamless connectivity.
3. **Automation:** Created 1,000 users programmatically with PowerShell.

---

## 🔗 Resources
- **PowerShell Script:** [Download Script and `names.txt`](scripts/user_creation.zip)
- **VirtualBox:** [VirtualBox Official Website](https://www.virtualbox.org/)
- **Windows ISOs:** [Microsoft Evaluation Center](https://www.microsoft.com/en-us/evalcenter/)

---

## Contact
For questions or feedback, feel free to reach out:
- **Email:** [Your Email Address]
- **LinkedIn:** [Your LinkedIn Profile]

---

## Screenshots Folder
Place all screenshots in the `screenshots/` folder to keep the repository organized. Ensure screenshots match the filenames referenced above.
