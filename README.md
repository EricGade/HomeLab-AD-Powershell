
<h1>Home Lab: AD & PowerShell (Hyper-V)</h1>


<h2>Description</h2>
This project provides a step-by-step guide on setting up a basic home lab with Active Directory using Hyper-V Manager. You will learn how to create virtual machines for both Windows Server and a Windows 10 OS client, set up Active Directory, add users using PowerShell, and join the Windows 10 OS client to the Windows Server domain. This guide is ideal for users who want to practice and test Active Directory and PowerShell in a virtualized environment. It also simulates how many corporate IT systems are structured.
<br />

<h2>Languages and Utilities Used</h2>

- **Windows Server 2016** (for Active Directory setup)
- **Hyper-V Manager** (virtualization software)
- **PowerShell** (for adding users to Active Directory)
- **Command Prompt** (optional for troubleshooting)
- **Windows 10/11** (for host machine)
  
<h2>Environments Used</h2>

- **Windows 11 Pro/Enterprise** 22H2 (for host machine)


<h2>Prerequisites</h2>

- Hypver installed on your host machine.
- Windows Server ISO for the virtual machine.
- Basic understanding of Active Directory and PowerShell commands.
- Ensure that virtualization is enabled in your system BIOS/UEFI settings.

<h2>Walk-through steps:</h2>

<b>Open Windows Features:</b>
- To open Windows Features, you can click the magnifying glass icon in the taskbar, search for "Windows Features," and open it when it appears in the search results.

<p align="center">
<img src="https://imgur.com/mu3m4lp.png" height="80%" width="80%" alt="Enable Windows Features"/>
<br/>
<br/>
<img src="https://imgur.com/3NnrxAG.png" height="80%" width="80%" alt="Enable Windows Features"/>
<br />
<br />
</p>
  
---
  
<b>Enable Hyper-V:</b>
- To enable Hyper-V, once the Windows Features window is open, look for "Hyper-V," check the box next to it, and then click "OK" to apply the settings.
<p align="center">
<img src="https://imgur.com/4VOrxqu.png" height="80%" width="80%" alt="Enable Hyper-V"/>
<br />
<br />
</p>
 
---
  
<b>Restart the Computer:</b>
- Once the settings are applied, restart your computer.
<p align="center">
<img src="https://imgur.com/e3cBk5u.png" height="80%" width="80%" alt="Restart Windows"/>
<br />
<br />
</p>
  
---
  
<b>Access Hyper-V Manager:</b>
- Log back into your computer, and using the magnifying glass icon, search for "Hyper-V" and open it.
- Alternatively, you can open Command Prompt and type `systeminfo` to check if Hyper-V is installed on your device.
<p align="center">
<img src="https://imgur.com/NmWhEi4.png" height="80%" width="80%" alt="Open Hyper-V Manager"/>
<br />
<br />
<img src="https://imgur.com/Go1wZyF.png" height="80%" width="80%" alt="Open Hyper-V Manager"/>
<br />
<br />
</p>


---

<b>Create a Test Virtual Machine:</b>
- Once Hyper-V is open, follow the on-screen instructions to connect your local machine to Hyper-V. 
- Next, right-click on the local machine, select **New**, and then click **Virtual Machine** to start creating a virtual machine. 
- Finally, follow the setup wizard to create a test virtual machine.
  
<p align="center">
<img src="https://imgur.com/ov5Txuu.png" height="80%" width="80%" alt="Create Virtual Machine"/>
<br />
<br />
<img src="https://imgur.com/g8owbuj.png" height="80%" width="80%" alt="Create Virtual Machine"/>
<br />
<br />
<img src="https://imgur.com/BqTeGs0.png" height="80%" width="80%" alt="Create Virtual Machine"/>
</p>

---

<h2>Conclusion</h2>

- You have now successfully installed Hyper-V and created a virtual machine.
- Note: The virtual machine will not function until an operating system (OS) is added and installed. Ensure you have the OS installation media (e.g., ISO file) ready to complete the setup.


