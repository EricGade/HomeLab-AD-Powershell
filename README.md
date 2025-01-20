# Home Lab: AD & PowerShell (Hyper-V)

## Description
This tutorial provides a step-by-step guide on setting up a basic home lab with an Active Directory (AD) using Hyper-V Manager and creating 1,000 users in AD with PowerShell.

## Languages and Utilities Used
- Windows Features  
- PowerShell  
- Command Prompt  
- Hyper-V Manager  

## Environments Used
- Windows 11 Pro/Enterprise (22H2)  

## Files You Need to Download
[DOWNLOAD NOW](#)

---

## Steps Included
1. **Create two virtual machines**
2. **Install & configure AD, RAS/NAT, and DHCP**
3. **Create 1,000 users in AD with PowerShell**
4. **Join Windows clients to the domain**
5. **Log in to the client machine with a created user**

---

## Walk-through Steps

### Step 1 – Create Two Virtual Machines
Watch my video on how to create the two virtual machines: [YouTube.com](#)

### Step 2 – Install & Configure AD, RAS/NAT, and DHCP
Watch my video on how to install and configure AD, RAS/NAT, and DHCP: [YouTube.com](#)

### Step 3 – Create 1,000 Users in AD with PowerShell
If you haven't already, download the PowerShell script: [DOWNLOAD NOW](#).

1. Extract the zip file on your host PC.
2. COPY the **AD_PS-master** folder from your host PC then go to the Windows Server 2016 virtual machine and PASTE. It really that simple trust me.


3. Open **PowerShell ISE** as an administrator and load the `1_CREATE_USERS` file from the **AD_PS-master** folder.
4. Run the following commands before executing the script:

   ```powershell
   Set-ExecutionPolicy Unrestricted
   cd C:\Users\a-egade\Desktop\AD_PS-master
   ls
   ```

   - `Set-ExecutionPolicy Unrestricted` (This allows the script to run without restrictions.)
   - `cd` to the correct folder location where the script is saved.
   - `ls` to verify the files in the folder.

5. Click the **Play** button in PowerShell ISE to run the script.

Your code should look something like this when creating new users:


### Step 4 – Join Windows Clients to the Domain
To join the client machine to the domain:

1. Ensure both the client and domain controller (DC) server are on the same **NIC (Network Interface Card).**
2. Once logged into the client machine, open **Command Prompt (CMD)** and run:
   ```cmd
   ipconfig
   ping mydomain.com
   ```
   - This verifies network settings and connectivity to the domain server.
   - The result should be as followed in the image.
     <img src="https://imgur.com/dazfCRo.png" height="80%" width="80%" alt="Join-PC"/>

3. Open **Settings > System > About > Rename this PC (Advanced) > Change.**
4. Under **Member of**, select **Domain** and enter **mydomain.com**.
5. Click **OK**, then enter your **Domain Controller (DC) credentials** when prompted.

<img src="https://imgur.com/TCWxw4a.png" height="80%" width="80%" alt="Join-PC"/>


### Step 5 – Log in to the Client Machine with a Created User
Now that all the steps are complete, we will test logging into the client machine with one of the created accounts:

1. Log out of the client machine.
2. Select **Other Users.**
3. Log in using one of the generated AD accounts for example below:
   
   - **Username:** `aabrev`  
   - **Password:** `Password1`
   
<img src="https://imgur.com/H9X18dO.png" height="80%" width="80%" alt="AD-Users"/>
<img src="https://imgur.com/1OmQIqp.png" height="80%" width="80%" alt="Client-Login-Screen"/>
<img src="https://imgur.com/dkC56WO.png" height="80%" width="80%" alt="Client-Logged-on"/>




If you can successfully log in with the AD account, your lab setup is complete! Additionally, since we configured **RAS/NAT**, the client machine should have internet access through the domain controller.

---

## 🎉 Congratulations! Your Home Lab setup is now complete.
  Full Video of the final Lab.
