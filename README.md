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

 <img width="1434" alt="Screenshot 2024-09-19 at 3 02 33 PM" src="https://github.com/user-attachments/assets/5f08c7e7-6a85-4b42-a204-13f0764b703f">

 Apply the Changes:

After selecting the necessary features, click "OK".
Windows will proceed to install and configure IIS with the selected components. This process may take a few minutes.

Verify IIS Installation:

- Once the installation is complete, you can verify that IIS is running by opening a web browser within your virtual machine and typing in  127.0.0.1 in the webbrowser.
- You should see the default IIS Welcome page, similar to this.

 <img width="1800" alt="Screenshot 2024-09-19 at 3 12 15 PM" src="https://github.com/user-attachments/assets/ef1f6ea9-8806-4f45-8114-14da5b7184ee">

Download PHP Manager for IIS:

- Navigate back to your installation files or download source.
- Locate the PHP Manager for IIS installation package.
- This file (PHPManagerForIIS_V1.5.0.msi)
- Download the latest version compatible with your system.
  
Run the Installer:

- Open the downloaded PHP Manager for IIS installer.
- Follow the installation wizard, agreeing to any license terms and selecting the appropriate installation options.
 
 <img width="1128" alt="Screenshot 2024-09-19 at 3 28 00 PM" src="https://github.com/user-attachments/assets/499b95e1-c882-4173-815f-05dc441dc853">
 
Return to the Installation Directory:

- Navigate back to the installation files where you previously obtained the PHP Manager for IIS.

Download the URL Rewrite Module:

- Locate the URL Rewrite Module installer.
- (rewrite_amd64_en-US.msi)
- Click on the "Download" button
- When it's done installing click finsih

<p><img width="1123" alt="Screenshot 2024-09-19 at 3 37 30 PM" src="https://github.com/user-attachments/assets/d466d497-e148-4aca-a710-c363081d9cdd">

Create a "PHP" Directory on the C: Drive

Open "This PC":

- Click on the "This PC" icon on your desktop or access it from the Start menu.
Navigate to the C: Drive:

- In the "This PC" window, locate and double-click on the "Local Disk (C:)" folder.
Create the "PHP" Folder:

- Inside the C: drive folder, right-click on an empty space.
From the context menu, select "New" and then click on "Folder".
Name the new folder "PHP" and press Enter to confirm.


<img width="1125" alt="Screenshot 2024-09-19 at 4 53 01 PM" src="https://github.com/user-attachments/assets/c6d694e4-7974-4be1-b4d1-4d53a653e6a8">

Extract the PHP Installation Files into the "PHP" Folder

Locate the PHP Zip File:

- Navigate to the installation directory where you downloaded the PHP zip file.

Open the Zip File:

- Double-click on the PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) file to open it.

Begin Extraction:

- In the zip file window, click on "Extract All..." to start the extraction process.
  
Select the Destination Folder:

- In the "Extract Compressed (Zipped) Folders" box, click on "Browse" to choose where to extract the files.
- Navigate to C:\ by selecting "This PC" and then "Local Disk (C:)".
- Choose the "PHP" folder you created earlier and click "Select Folder".



</p><img width="1123" alt="Screenshot 2024-09-19 at 5 03 28 PM" src="https://github.com/user-attachments/assets/581fc67c-e366-4bcd-a4d9-f9f3a40a4333">
<p>
</p>
<p>
</p>
<p>
<img width="1121" alt="Screenshot 2024-09-19 at 5 05 06 PM" src="https://github.com/user-attachments/assets/82e9642a-13c0-4205-a4c4-760eb3617bc8">

<p>

 Install the Visual C++ Redistributable Package from the Installation Package
 
Locate the Visual C++ Redistributable Installer:

- Navigate to the installation directory where you previously extracted the PHP files.
- Look for the Visual C++ Redistributable installer file (VC_redist.x86.exe.).
- Install the file 

 <img width="1124" alt="Screenshot 2024-09-19 at 5 13 33 PM" src="https://github.com/user-attachments/assets/734a16ae-11a6-4c3c-9ba5-72828c600bd8">
 <p>
</p>
<p>
</p>
<p>
<img width="480" alt="Screenshot 2024-09-19 at 5 14 00 PM" src="https://github.com/user-attachments/assets/d99ff3fa-23fb-4d1c-bffa-d0f4aed1bc57">

 Install the MySQl Package from the Installation Package
 
Locate the MySQL  Installer:

- Navigate to the installation directory where you previously extracted the PHP files.
- Look for the  MySQL installer file, typically named (mysql-5.5.62-win32.msi))

<img width="1121" alt="Screenshot 2024-09-19 at 5 21 32 PM" src="https://github.com/user-attachments/assets/ecef766a-413b-467e-b5b8-9394b06e49ea">


- Once you reach this page, select Typical, click Finish, and launch MySQL on your computer.

<img width="497" alt="Screenshot 2024-09-19 at 5 22 36 PM" src="https://github.com/user-attachments/assets/f30c30bc-68c4-4a2e-8864-0aa94af33b74">

- After launching MySQL, click Next and select Standard Configuration, leaving the subsequent options unchanged. 
- When prompted for a username and password, set both to root for simplicity, this is only for the lab please DO NOT do this  in real life. Please note these credentials for future use.
- After it is set please click execute. And finish


<img width="494" alt="Screenshot 2024-09-19 at 5 25 30 PM" src="https://github.com/user-attachments/assets/8f050bfb-4fad-4ec5-b25e-9eb9b99695e4">
 <p>
</p>
<p>
</p>
<p>
<img width="497" alt="Screenshot 2024-09-19 at 5 28 49 PM" src="https://github.com/user-attachments/assets/08b61739-abdb-429d-9251-330435a2023f">

 
Open IIS as an Administrator
Search for IIS:

- In the bottom-right corner of your screen, type "IIS" into the search bar.
  
Run IIS with Administrative Privileges:

- Once IIS appears in the search results, double-click on it.
- Click "Run as administrator" to launch IIS with the necessary administrative rights, allowing you to configure PHP for OsTicket.
<img width="782" alt="Screenshot 2024-09-19 at 5 38 45 PM" src="https://github.com/user-attachments/assets/b24631f5-8827-4207-af22-0ee83f934b29">
- This is what ISS admin should look like
  <img width="1335" alt="Screenshot 2024-09-19 at 5 53 07 PM" src="https://github.com/user-attachments/assets/6958d44b-0fd5-4cfa-a89e-8efd989df3e4">
   Register PHP with IIS
Open PHP Manager:

- In IIS Manager, navigate to the PHP Manager section.
- 
Register a New PHP Version:

- Click on "Register new PHP version".
- Browse to the PHP installation directory (e.g., C:\PHP) and select the php-cgi.exe file.
- Click "OK" to complete the registration.
  
<img width="1336" alt="Screenshot 2024-09-19 at 5 55 03 PM" src="https://github.com/user-attachments/assets/1f638417-b3ef-4d06-a5f4-2decc38bce10">

Click the three dots(...) to browse

<img width="508" alt="Screenshot 2024-09-19 at 5 56 08 PM" src="https://github.com/user-attachments/assets/4a6b4014-11ea-4577-ac12-22b393e06ad9">


</p>
<br />

