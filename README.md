# IT Lab Portfolio

## Project Overview
A virtual IT lab environment built in VirtualBox. Includes Windows 10 installation, local account creation, VM hardware configuration, and a Windows Server 2022 domain environment.

---

## Screenshots and Captions

### VirtualBox VM Setup
- ![VM Settings](screenshots/ServerVMSetup.png)  
  *Overview of the VirtualBox VM hardware configuration, including RAM, CPU, storage, and network settings.*

- ![VM Hardware](screenshots/ServerVMHardware.png)  
  *Adjusting the VM's base memory (2048 MB) and processors (2) for optimal lab performance.*

- ![VM Hard Disk](screenshots/ServerVMHardDisk.png)  
  *Creating a new virtual hard disk (VDI, dynamically allocated) of 60 GB for Windows Server 2022 installation.*

- ![VM Setup](screenshots/ServerVMSetup2.png)  
  *Initial setup summary in VirtualBox, showing VM creation details.*

---

### Windows 10 Installation & Setup
- ![Windows 10 Edition Selection](screenshots/VMSelections.png)  
  *Choosing the Windows 10 Pro (x64) edition during installation.*

- ![Local Account Creation](screenshots/VMAccountCreation.png)  
  *Setting up a local account name for the Windows 10 VM.*

- ![Local Account Password](screenshots/VMPassword.png)  
  *Creating a strong password for the local account.*

- ![First Boot](screenshots/VMFirstBoot.png)  
  *First boot of the Windows 10 desktop environment, showing successful VM setup.*

---

### Windows Server 2022 Domain Controller

#### Overview
- Windows Server 2022 Core (no GUI).
- Configured as the domain controller for the `testlab.local` domain.
- Connected to the client VM in an internal network for isolated domain testing.

#### Key Steps
- Set static IP for the Server Core: `192.168.56.10`.
- Installed Active Directory Domain Services (ADDS).
- Created a new Organizational Unit (`Employees`) and a user (`jdoe`).
- Joined the client VM to the `testlab.local` domain.
- Configured firewall rules for ICMPv4 (ping).

---

#### Screenshots and Captions

- ![Server IP Config](screenshots/ServerVMSetCustomIP.png)  
  *Server Core static IP setup using PowerShell.*

- ![Server Domain Setup](screenshots/ServerVMSetDomainController.png)  
  *Installing Active Directory Domain Services and creating the `testlab.local` domain.*

- ![OU and User](screenshots/ServerVMOUandUSER.png)  
  *Creating the `Employees` organizational unit and adding `John Doe` as a domain user.*

- ![Client Domain Join](screenshots/ServerVMConnection.png)  
  *Joining the Windows 10 client to the `testlab.local` domain.*

- ![Firewall Rule](screenshots/createnewrule.png)  
  *Adding an inbound firewall rule for ICMPv4 (ping) on the client VM.*

- ![Domain Join Confirmation](screenshots/connection.png)  
  *Client VM successfully joined to the `testlab.local` domain.*

---

### Skills Learned
- VirtualBox VM creation and hardware resource allocation.
- Clean installation of Windows 10 in a virtual environment.
- Setting up local user accounts for lab usage.
- Static IP and DNS configuration via PowerShell in Server Core.
- Installing and configuring Active Directory Domain Services.
- Creating and managing Organizational Units and users in AD.
- Configuring Windows Firewall rules to enable domain communication.
- Joining a Windows 10/11 client to an Active Directory domain.

---

## Final Lab State
✅ Domain controller (`testlab.local`) operational.  
✅ Client joined to domain.  
✅ Inbound ping (ICMPv4) working for connectivity testing.  
✅ Ready for further lab testing (GPOs, file sharing, DNS, etc.).

---

