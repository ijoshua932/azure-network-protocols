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

![image](https://github.com/ijoshua932/azure-network-protocols/assets/139269375/eab133da-405d-4397-8de3-d1c6c8576bc7)

![image](https://github.com/ijoshua932/azure-network-protocols/assets/139269375/64ddb5bd-ad38-47d8-b142-6c7f04417b73)

</p>
<p>
To ping and observe ICMP traffic between two VMs, first, ensure that both VMs are running on the same network or virtual network within Azure. Open Comand Prompt or PowerShell on one VM, use the "ping" command followed by the IP address or hostname of the other VM to send ICMP packets. On the destination VM, use tools like Wireshark to capture and analyze the incoming ICMP traffic.
</p>
<br />

<p>

![image](https://github.com/ijoshua932/azure-network-protocols/assets/139269375/50d5190d-a7bf-4944-ab86-95f082668584)

![image](https://github.com/ijoshua932/azure-network-protocols/assets/139269375/e2256975-165c-4021-9f97-a103d9aaad36)

</p>
<p>
When the inbound Network Security Group (NSG) is changed to deny ICMP traffic, the ping command between two VMs will be interrupted. This is because ICMP traffic will be blocked at the network level, preventing the VMs from exchanging ICMP echo requests and replies. As a result, the ping command will show no responses or timeouts, indicating the communication is blocked by the NSG rules.
</p>
<br />

<p>

![image](https://github.com/ijoshua932/azure-network-protocols/assets/139269375/2a98e6bf-045e-47dd-9568-08eb44f061e3)
</p>
<p>
Reversing the Network Security Group (NSG) rule to allow ICMP traffic, restores the ability to use the ping command between the two VMs. By changing the rule to permit ICMP traffic, the NSG allows the necessary ICMP echo requests and replies to pass through the network, enabling the VMs to communicate with each other using the ping command again.
</p>
<br />

<p>

![image](https://github.com/ijoshua932/azure-network-protocols/assets/139269375/97348836-93b5-4a49-abe8-5616e7d64e47)

</p>
<p>
To observe DNS traffic of www.google.com, filter the captured packets by DNS protocol, and then access www.google.com in your web browser or use the "nslookup" command in the command prompt to generate DNS traffic for google.com. Wireshark will display the captured DNS packets related to the communication with www.google.com.
</p>
<br />

<p>
  
![image](https://github.com/ijoshua932/azure-network-protocols/assets/139269375/14f59c9f-f3ab-43c2-8298-1ae7860a810b)

</p>
<p>
To observe DNS traffic of www.disney.com, filter the captured packets by DNS protocol, and then access www.disney.com in your web browser or use the "nslookup" command in the command prompt or terminal to generate DNS traffic for www.disney.com. Wireshark will display the captured DNS packets related to the communication with google.com.
</p>
<br />
