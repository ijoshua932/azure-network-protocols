<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Create Resourses
- Configure VMs
- Instal WireShark
- Observe ICMP Traffic
- Observe DNS Traffic

<h2>Actions and Observations</h2>

<p>

![image](https://github.com/ijoshua932/azure-network-protocols/assets/139269375/9c034adb-d8d2-4520-87f3-1ad09ae135f4)
</p>
<p>
To create a resource group in Azure, log in to the Azure Portal with your account. Navigate to the "Resource groups" section, click "Create," provide a unique name, select the desired subscription, choose a region, and click "Review + Create." Finally, click "Create" to create the resource group.
</p>
<br />

<p>

![image](https://github.com/ijoshua932/azure-network-protocols/assets/139269375/084f937e-a88c-45fe-b296-ebad52e650fb)
</p>
<p>
To create two virtual machines (VMs) in Azure, one with Windows and one with Linux, first, navigate to the Azure Portal. Go to "Virtual machines," click "Add," select "Windows Server" for the Windows VM and "Linux" for the Linux VM. Configure the settings such as VM name, region, size, authentication, and then click "Create" to provision both VMs simultaneously.
</p>
<br />

<p>

![image](https://github.com/ijoshua932/azure-network-protocols/assets/139269375/169ea2ce-7645-4ced-a42e-020ab49af878)
</p>
<p>
To install Wireshark, download the appropriate installer for your operating system from the official Wireshark website. Run the installer and follow the on-screen instructions to complete the installation process. Once installed, you can launch Wireshark to start capturing and analyzing network packets.
</p>
<br />

<p>


</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>


</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>


</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
