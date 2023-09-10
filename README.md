<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com/watch?v=lzHRxxSmQXc)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Setup Resources in Azure
- Ensure Connectivity between the client and Domain Controller
- Install Active Directory
- Create an Admin and Normal User Account in AD
- Join Client-1 to your domain (mydomain.com)
- Setup Remote Desktop for non-administrative users on Client-1
- Create a bunch of additional users and attempt to log into client-1 with one of the users 

<h2>Deployment and Configuration Steps</h2>

<p>
  
![image](https://github.com/techwiz77777/configue-ad/assets/143854558/43e840bc-6080-4a1b-adaa-7d201f288fa9)
![image](https://github.com/techwiz77777/configue-ad/assets/143854558/7bf9f5ae-c58d-4e22-8017-eb3c417af838)
</p>
<p>
Here we are creating are resource groups along with setting the domain controller's IP address to "static".
</p>
<br />

<p>
  
![image](https://github.com/techwiz77777/configue-ad/assets/143854558/03594549-3ce6-43e8-b182-51bac1b7b82e)
![image](https://github.com/techwiz77777/configue-ad/assets/143854558/1359d6c9-fcd1-446c-a34e-4e2dfa0bd275)
![image](https://github.com/techwiz77777/configue-ad/assets/143854558/b1a603b2-4989-4c81-9b1b-effbdead0c64)
![image](https://github.com/techwiz77777/configue-ad/assets/143854558/c68446a9-2c24-4f82-b7c4-5b443b9722b9)
![image](https://github.com/techwiz77777/configue-ad/assets/143854558/47ae7d2c-c832-4b4c-a749-f93a1cd593a1)

</p>
<p>
Here we are pinging DC-1 IP address to make sure that there's a connection, then enable ICMPv4 in on the local windows Firewall. Afterwards, we install Active Directory, set up a new forest as mydomain.com then log in as DC-1  mydomain.com\labuser. 
</p>
<br />

<p
  
![image](https://github.com/techwiz77777/configue-ad/assets/143854558/57640166-d958-4986-a965-86119f611067)
![image](https://github.com/techwiz77777/configue-ad/assets/143854558/e33f3257-70bf-4943-8dd9-473a3b0f0103)
![image](https://github.com/techwiz77777/configue-ad/assets/143854558/2e4a587d-8ef4-4cac-b4bb-9a60f4c40e63)
![image](https://github.com/techwiz77777/configue-ad/assets/143854558/2e921169-a50a-4b70-bea7-210c91407ef3)

</p>
<p>
Here we create an organizational group for employees and admins then join Client-1 to mydoamin to setup Remote Desktop for non-administrative users on Client-1 as well. Afterwars, we create additional users to log into Client-1.

</p>
<br />
