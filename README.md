# Home Lab: Active Directory AD & PowerShell 

## Description
This tutorial provides a step-by-step guide on setting up a basic home lab with an Active Directory (AD) using Hyper-V Manager and creating 1000 users in AD with PowerShell.

## Languages and Utilities Used
- PowerShell
- Command Prompt
- Hyper-V Manager

## Environments Used
- Windows 11 Pro/Enterprise (22H2)

## Files You Need to Download
- [Win Server 2016 Download](https://info.microsoft.com/ww-landing-windows-server-2016.html)
- [Windows 10 ISO Download](https://www.microsoft.com/en-us/software-download/windows10)
- [AD_PS-master Download file](https://github.com/EricGade/HomeLab-AD-Powershell/blob/main/AD_PS-master.zip)

## Steps Included
1. Virtual Machines Setup
    - Create 2 Virtual Switches ("NAT" and "SUBNETA")
    - Create 2 Virtual Machines ("DC1" and "Client1")
2. Install & Configure AD, RAS/NAT, DHCP
3. Create 1000 Users in AD using PowerShell
4. Join "Client1" to the Domain
5. Log in to "Client1" with a Created User

## Walk-through Steps

### Step 1: Virtual Machines Setup
#### Create 2 Virtual Switches ("NAT" and "SUBNETA")
Open Hyper-V Manager. Right-click on the local machine and select **Virtual Switch Manager**. Alternatively, select **Virtual Switch Manager** from the Action pane.

Next, click on **New Virtual Network Switch** and create two virtual switches:
- **NAT** (External)
- **SUBNETA** (Private)
  
![Virtual Switch Manager Open](https://imgur.com/6bGexoi.png)

#### Create 2 Virtual Machines ("DC1" and "Client1")
1. Configure the Virtual Machine settings to match the summary shown below.
2. Attach **Windows Server 2016 ISO** to the **DC1** virtual machine.
   
![Virtual Machine Settings](https://imgur.com/ZdZtpFk.png)

#### Configure DC1 Network Adapters
1. Right-click on **DC1**, select **Settings**.
2. Add a second network adapter:
    - **NAT** for external access
    - **SUBNETA** for internal network
      
![Virtual Machine Settings](https://imgur.com/BpG2ZDi.png)

#### Install Windows Server 2016 on DC1
1. Start **DC1** and install **Windows Server 2016**.

#### Rename Computer in DC1
1. Open **System Properties** in **DC1**.
2. Click **Change** next to the computer name.
3. Rename the computer to **DC1**.
4. Restart the machine to apply the changes.

#### Rename Network Adapters in DC1
1. Open **Network Settings** in **DC1**.
2. Rename **NAT** and **SUBNETA** for easy identification.
   
![Virtual Machine Settings](https://imgur.com/6RUafEc.png)

#### Set Static IP Address for SUBNETA (Private Network) in DC1

1. Open **Network Settings** on **DC1**.
2. Locate the **SUBNETA (Private Network)** adapter, right-click on it, and select **Properties**.
3. In the list of items, select **Internet Protocol Version 4 (TCP/IPv4)**, then click **Properties**.
4. Select **Use the following IP address** and enter the following values:
   - **IP address:** `172.16.0.1`
   - **Subnet mask:** `255.255.255.0`
   - **Preferred DNS server:** `127.0.0.1`
5. Click **OK** to save the settings and close the dialog.
   
![Virtual Machine Settings](https://imgur.com/tAnqObi.png)

#### Create Client1 Virtual Machine
1. Repeat the steps to create a new Virtual Machine named **Client1**.
2. Connect **Client1** to **SUBNETA**.
3. Attach **Windows 10 ISO** and install **Windows 10 Pro**.

![Virtual Machine Settings](https://imgur.com/rYM9hiw.png)

#### Install Windows 10 on Client1
1. Complete the Windows 10 installation on **Client1**.

#### Rename Computer in Client1
1. Open **System Properties** in **Client1**.
2. Click **Change** next to the computer name.
3. Rename the computer to **Client1**.
4. Restart the machine to apply the changes.

## Video Walkthrough
[Watch the Video](https://www.youtube.com/watch?v=dQw4w9WgXcQ)

## Next Steps
- Step 2 – Install & Configure AD, RAS/NAT, DHCP
- Step 3 – Create 1000 Users in AD with PowerShell
- Step 4 – Join **Client1** to the Domain
- Step 5 – Login to **Client1** as a Created User


