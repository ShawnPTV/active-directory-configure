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

<h2>Operating Systems Used </h2>

- Windows Server 2025
- Windows 11 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1: Deploy azure virtual machines- create a windows server 2025 virtual machine to serve as the domain controller. create a windows 11 client virtual machine configure the virtual network, subnet mask, and network security settings to allow required communication between the machines.
- Step 2: install and configure active directory- Install the active directory domain services(AD DS) role on the windows server.
- Step 3: create users and configure the domain- create organizational units(OUs), user accounts, and security groups in active directory
- Step 4: test and verify active directory sign in to the windows 11 client using a domain user account. verify domain connectivity, dns resolution, and user authentication

<h2>Deployment and Configuration Steps</h2>

<p>
<img width="2430" height="1686" alt="image" src="https://github.com/user-attachments/assets/7d889ffa-c6cf-496b-b2da-dddb3da4e23a" />

</p>
<p>
In this figure: Installing and verifying active directory domain services and DNS roles in windows server manager. I had it installed already from a recent lab but this is one of the early steps in configuring active directory
</p>
<br />
 />
<img width="2308" height="1364" alt="image" src="https://github.com/user-attachments/assets/11755b78-f000-47b0-8636-b1ed0c7f9f55" />
<img width="2308" height="1364" alt="image" src="https://github.com/user-attachments/assets/f6cbe700-b1b0-4ad9-9ef0-fb36878727bb" />

</p>
<p>
Configured Active Directory Users and computers to manage user accounts and organize resources within the mydomain.com domain. created and organized organizational units (OUs) including _ADMINS, _CLIENTS, _EMPLOYEES, and _GROUPS, to seperate users, computers, and administrative resources.
</p>
<br />
<img width="1462" height="1184" alt="image" src="https://github.com/user-attachments/assets/dfc48ccf-81e8-47d0-bdff-86c131358163"
 /><img width="1884" height="1192" alt="image" src="https://github.com/user-attachments/assets/ba4e9b0a-c5a2-411d-8f3a-4bad0510c91f"
 /><img width="1884" height="1192" alt="image" src="https://github.com/user-attachments/assets/56c8ddb9-95e0-403a-a904-f8593fae0209"
 />
 />
 />


<p><img width="1980" height="1308" alt="image" src="https://github.com/user-attachments/assets/7efcb9c9-c2d4-4f85-a18c-032aba19e245" />
<img width="2226" height="1256" alt="image" src="https://github.com/user-attachments/assets/b218a5fc-89ff-45ac-be61-bf8d0b1ffc3a" />

Tested active directory configuration by reviewing the windows user account and using PowerShell to verify DNS resolution for the domain (i have a accident with the command prompt showing a non existent domain because i changed the dns but it still is connected to the dc-1-domain controller vm)
</p>
<br />
