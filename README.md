<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azure Virtual Machine
- Internet Information Services (IIS)
- PHP Manager
- Rewrite Module
- VC Redist
- MySQL
- Heidi SQL
- osTicket v1.15.8
- Link to downloads: https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6


- 

<h2>Installation Steps</h2>

<p>

 Create a Virtual Machine:

Visit the Azure Portal: Navigate to https://portal.azure.com/.

Create a New Resource Group:

- In the Azure Portal, go to the "Resource Groups" section.
- Click on "Add" to create a new resource group.
- Provide a name for your resource group and select a region.

Name Your Virtual Machine:

- In the Azure Portal, click on "Create a resource".
- Select "Virtual Machine" from the list of available resources.
- Enter a unique name for your virtual machine.

<img width="858" alt="Screenshot 2024-09-19 at 1 38 56 PM" src="https://github.com/user-attachments/assets/d670844e-fbe5-45c9-b008-418a38981554">

Set Up Your VM:

- Configure your virtual machine with Windows 10 Pro, version 22H2.
- Allocate at least 2 vCPUs and 16 GB of memory to ensure optimal performance.
- Review and adjust any additional settings as needed, then proceed to create the VM.
<img width="858" alt="Screenshot 2024-09-19 at 1 53 40 PM" src="https://github.com/user-attachments/assets/8dcc1678-d607-4207-8503-3dd0e46f9b52">


Connect to Your Virtual Machine:

- Retrieve the Public IP Address: Once your VM is created, locate and note the public IP address assigned to it in the Azure Portal.


- Use Remote Desktop: Open the Remote Desktop Connection application on your local machine. (Downloand Microsoft remote desktop on mac from app store)

- Establish the Connection: Click the + icon add PC and enter the VM's public IP address in the Remote Desktop app.

- Enter password: Enter your previously made username and password.

<img width="1407" alt="Screenshot 2024-09-19 at 2 06 03 PM" src="https://github.com/user-attachments/assets/3f54c539-e49f-4dd2-914b-42f639ee60b4">
</p>
<p>
</p>
<p>
<img width="458" alt="Screenshot 2024-09-19 at 2 33 00 PM" src="https://github.com/user-attachments/assets/9c525d6b-5711-44c8-8859-2dc5313bc2b3">

After connecting to your virtual machine:

- Access the Control Panel: Locate the Control Panel icon in the bottom-left corner of the screen and click on it.
  
- Navigate to Programs: In the Control Panel, select "Programs".

- Modify Windows Features: Click on "Turn Windows features on or off" to manage and adjust the Windows features as needed.

<img width="789" alt="Screenshot 2024-09-19 at 2 26 35 PM" src="https://github.com/user-attachments/assets/33bc98ee-fbe3-4397-a314-ae68a6fc9b7e">
<p>
</p>
<p>
<img width="1120" alt="Screenshot 2024-09-19 at 2 39 09 PM" src="https://github.com/user-attachments/assets/bae4bafd-72c9-4837-ab68-19600bbd8952">
<p>
</p>
<p>
<img width="1122" alt="Screenshot 2024-09-19 at 2 42 02 PM" src="https://github.com/user-attachments/assets/58e79646-5a20-4070-9e01-9527e10acf4b">

Access Application Development Features:

- Under "World Wide Web Services", expand the "Application Development Features" node.

  
Enable CGI and Common HTTP Features:

Check the Boxes:
- CGI: Locate and check the box next to "CGI" to enable Common Gateway Interface support.
- Common HTTP Features: Ensure that "Common HTTP Features" is also checked.

- <img width="1434" alt="Screenshot 2024-09-19 at 3 02 33 PM" src="https://github.com/user-attachments/assets/5f08c7e7-6a85-4b42-a204-13f0764b703f">

<p>
</p>
<p>


 
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
