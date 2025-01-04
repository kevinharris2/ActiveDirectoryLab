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

### Step 1: Install VirtualBox and Download ISOs
<p align="center">
<img src="https://imgur.com/0yhIQMk.png" alt="VirtualBox Installation" width="80%" height="80%" />
</p>

- Choose the ISO download for your language
<p align="center">
<img src="https://imgur.com/mWB3OTG.png" alt="VirtualBox Installation" width="80%" height="80%" />
</p>

---

### Step 2: Create the Domain Controller VM
- Customize your VM in settings
- You can right click to clone your VM along with its settings
<p align="center">
<img src="https://imgur.com/GHEaUvl.png" alt="Domain Controller Configuration" width="80%" height="80%" />
</p>

---

### Step 3: Install Windows Server 2019
<p align="center">
<img src="https://imgur.com/15xaMnl.png" alt="Windows Server Installation" width="80%" height="80%" />
</p>

- Select custom Installation. The server will restart a couple times after selecting next
- Create a easy to remember password when prompted

<p align="center">
<img src="https://imgur.com/tYbnCtZ.png" alt="Windows Server Installation" width="80%" height="80%" />
</p>

- Unlock the sign in screen by selecting Input > keyboard > Insert Ctrl-alt-delete

<p align="center">
<img src="https://imgur.com/QBqkeQy.png" alt="Windows Server Installation" width="80%" height="80%" />
</p>
---

### Step 4: Configure the Domain Controller
#### Assign Static IPs
<p align="center">
<img src="https://imgur.com/n8phUHS.png" alt="IP Configuration" width="80%" height="80%" />
</p>

<p align="center">
<img src="https://imgur.com/Vvur0AN.png" alt="IP Configuration" width="80%" height="80%" />
</p>

#### Install Active Directory Domain Services. AD DS

- Select 'Add role and features'
<p align="center">
<img src="https://imgur.com/EB5V23d.png" alt="Active Directory Installation" width="80%" height="80%" />
</p>

- Check Active Directory Domain Services and select next> install.

<p align="center">
<img src="https://imgur.com/Ubv04n1.png" alt="Active Directory Installation" width="80%" height="80%" />
</p>

- In the upper right corner of your screen select Post Deployment configuration
  
<p align="center">
<img src="https://imgur.com/2SIyS4I.png" alt="Active Directory Installation" width="80%" height="80%" />
</p>

- Install and create dedicated admin account.

<p align="center">
<img src="https://imgur.com/bM9cQN3.png" alt="Active Directory Installation" width="80%" height="80%" />
</p>


<p align="center">
<img src="https://imgur.com/MxIvoTa.png" alt="Active Directory Installation" width="80%" height="80%" />
</p>

### Step 5: Install remote access and network address translation RAS / NAT
<p align="center">
<img src="https://imgur.com/BtfGGMt.png" alt="Active Directory Installation" width="80%" height="80%" />
</p>

- Select NAT in configurations
<p align="center">
<img src="https://imgur.com/rGIKw9O.png" alt="Active Directory Installation" width="80%" height="80%" />
</p>

### Step 6: Install and configure DHCP server. 
<p align="center">
<img src="https://imgur.com/v9C3bi8.png" alt="Active Directory Installation" width="80%" height="80%" />
</p>

- Identify IP address range
<p align="center">
<img src="https://imgur.com/nX9NvSm.png" alt="Active Directory Installation" width="80%" height="80%" />
</p>

<p align="center">
<img src="https://imgur.com/orfP92c.png" alt="Active Directory Installation" width="80%" height="80%" />
</p>
---

### Step 7: Automate User Creation with PowerShell

### extract and then open 'names' plain text file 
#### Edit `names.txt` File
<p align="center">
<img src="https://imgur.com/1OFOhZK.png" alt="Editing Names File" width="80%" height="80%" />
</p>

#### Run the PowerShell Script
<p align="center">
<img src="https://imgur.com/LbiwH45.png" alt="Editing Names File" width="80%" height="80%" />
</p>


---

### Step 8: Create the Client VM
<p align="center">
<img src="https://imgur.com/JO2bfHE.png" alt="Client VM Configuration" width="80%" height="80%" />
</p>
- Name the Vm 'CLIENT1'and make sure adapter 1 is attached to 'Internal network' You can edit the clone server you made earlier 
---

### Step 9: Join the Client to the Domain
<p align="center">
<img src="INSERT_LINK_TO_STEP9_IMAGE" alt="Joining Client to Domain" width="80%" height="80%" />
</p>

---

### Step 10: Verify Connectivity
#### Check Network Configuration
<p align="center">
<img src="INSERT_LINK_TO_STEP10_IMAGE" alt="Verifying Network Configuration" width="80%" height="80%" />
</p>

#### Log in with a Domain Account
<p align="center">
<img src="INSERT_LINK_TO_STEP11_IMAGE" alt="Logging in with Domain Account" width="80%" height="80%" />
</p>

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
- Place all screenshots in the `screenshots/` folder.
- Replace `INSERT_LINK_TO_STEPX_IMAGE` with the appropriate file path or URL to your `.png` images.

