<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell
- Command Line

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Create two virtual machines one running Windows Server (Domain Controller) and the other running Windows 10. Make sure the VMs are on the same virtual network.
- Set the Domain Controller to have a static private IP Address.
- Ensure connectivity between the two virtual machines. 
- Install Active Directory onto the Domain Controller.
- Create an Admin user and non-admin user in your Active Directory.
- Join your other virtual machine the client to the Domain.
- Setup your client to allow non-admin users to use remote desktop.
- Run a script to create many additional users to test remote desktop functionality.

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/xiyEKiE.png"/>
</p>
<p>
Create two virtual machines in Azure; One with Windows server and the other running Windows 10. Ensure both are using two cores then ensure they are both on the same network using network watcher and using the topology feature shown on the left side of the screen in the Azure portal interface.
</p>
<br />

<p>
<img src="https://i.imgur.com/xNnthv2.png"/>
</p>
<p>
The virtual machine with Windows server installed will be the Domain Controller and is called DC-1 in this example. From the virtual machine page go to networking and then click the text next to network interface to continue with the demonstration.
</p>
<br />

<p>
<img src="https://i.imgur.com/i9Tk1uA.png"/>
</p>
<p>
From the network interface page click on ip configurations and then ipconfig1 to set the IP to static.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


<p>
<img src="https://i.imgur.com/UquyD5f.png"/>
</p>
<p>
Open the client on remote desktop and from a command line type in ping -t and then the Domain Controller's private IP address. This will lead to a request time out. To enable traffic go onto the server and go to windows firewall with advance security maximize the window then click on inbound rules sort by protocol and then enable the first two ICMPv4 rules. 
</p>
<br />

<p>
<img src="https://i.imgur.com/omCtZl9.png"/>
</p>
<p>
To install active directory click on server manager and then to add roles and features.
</p>
<br />


<p>
<img src="https://i.imgur.com/2tFcTMb.png"/>
</p>
Click next until you get to this window and make sure to install Active Directory Domain Services.
<p>

<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

