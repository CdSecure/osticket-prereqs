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

Register a New PHP Version:

- Click on "Register new PHP version".
- Browse to the PHP installation directory (e.g., C:\PHP) and select the php-cgi.exe file.
- Click "OK" to complete the registration.
  
<img width="1336" alt="Screenshot 2024-09-19 at 5 55 03 PM" src="https://github.com/user-attachments/assets/1f638417-b3ef-4d06-a5f4-2decc38bce10">

Click the three dots(...) to browse

<img width="508" alt="Screenshot 2024-09-19 at 5 56 08 PM" src="https://github.com/user-attachments/assets/4a6b4014-11ea-4577-ac12-22b393e06ad9">
 <p>
</p>
<p>
</p>
<p> 
<img width="885" alt="Screenshot 2024-09-19 at 5 58 23 PM" src="https://github.com/user-attachments/assets/0c4f3b98-0be0-416d-9345-3fe74758d8d6">
Restart the Web Server (IIS)
 
Navigate to the OsTicket Tab:

- Click on the OsTicket tab located at the top-left corner of the interface.
  
Initiate stop and start:

- On the right side of the OsTicket tab, you will see a start and stop  button.
- Click the stop button to restart the IIS web server.
- Click the start button to restart the server.
  
<img width="1332" alt="Screenshot 2024-09-19 at 6 00 50 PM" src="https://github.com/user-attachments/assets/67f8a0d1-f8e4-45de-bdf6-118f379bc235">

 Install OsTicket
Return to the OsTicket Installer:

- Navigate back to the OsTicket installer.
  
Locate and Extract the Installer File:

- Find the OsTicket installer file within the installation package.
- Click on the OsTicket folder and select "Extract" to unzip the installer.

<img width="1123" alt="Screenshot 2024-09-20 at 12 29 33 PM" src="https://github.com/user-attachments/assets/3354b1ea-5134-41da-be68-5390d09cc6ea">

<p>
</p>
<p>
</p>
<p> 
<img width="1116" alt="Screenshot 2024-09-20 at 12 29 54 PM" src="https://github.com/user-attachments/assets/1fa2c38f-26cd-4e62-b71d-1b1e493a4466">


Access the Extracted Folders:

- Once extraction is complete, open the extracted OsTicket folder.
- You will see two folders inside.
  
Copy Installer Files to the Web Server Folder:

- Copy the necessary files from the extracted folders.
- Go to Window C->inetpub->wwwroot.
- Click into wwroot and drag the upload folder into it.

<img width="1122" alt="Screenshot 2024-09-20 at 12 33 23 PM" src="https://github.com/user-attachments/assets/6b872296-d07f-48e0-a379-54ffe0d972d1">
<p>
</p>
<p>
</p>
<p> 
<img width="1148" alt="Screenshot 2024-09-20 at 12 49 55 PM" src="https://github.com/user-attachments/assets/cf9660c3-0df0-4821-9023-2d3c1b2e0d29">
<p>
</p>
<p>
</p>
<p> 
<img width="1128" alt="Screenshot 2024-09-20 at 12 55 07 PM" src="https://github.com/user-attachments/assets/780852a6-5a38-49b3-86fd-cef13d1a0d2c">

Rename the Folder:

- Right-click on the "upload" folder.
- Select "Rename" from the context menu.
- Change the folder name from "upload" to EXACTLY "osTicket".
- Press Enter to confirm the new name.

- 
<img width="1120" alt="Screenshot 2024-09-20 at 1 11 28 PM" src="https://github.com/user-attachments/assets/5455a58b-203e-40d1-9cfa-54d1a7d29b8d">


 Start and Stop IIS to Reload the Server
Open IIS Manager:

- In the bottom left corner type ISS and run as admin

Select Your Server:

- In the Connections pane on the left, click on your server name to select it.
  
Stop the IIS Server:

- In the Actions pane on the right, click on the "Stop" button to stop the IIS server.
- 
Start the IIS Server:

- After a moment, click on the "Start" button in the Actions pane to start the IIS server again.

<img width="1332" alt="Screenshot 2024-09-19 at 6 00 50 PM" src="https://github.com/user-attachments/assets/67f8a0d1-f8e4-45de-bdf6-118f379bc235">

Browse OsTicket in IIS

Navigate to the OsTicket Folder:

- In the Connections pane on the left, expand the Sites node.
- Click on "Default Web Site" to view its contents.
  
Select the OsTicket Directory:

- Click on the "osticket" folder within the Default Web Site.

Browse the OsTicket Application:

- In the Actions pane on the right, click the "Browse" link.
- This will open a web browser and navigate to your OsTicket installation.
- You should see something like below 
  
</p><img width="1332" alt="Screenshot 2024-09-20 at 1 17 37 PM" src="https://github.com/user-attachments/assets/f0a8b83f-21d3-4d7d-8d06-5fbf40c662b9">

<p>
</p>
<p>
</p>
<p> 
<img width="1205" alt="Screenshot 2024-09-20 at 1 29 40 PM" src="https://github.com/user-attachments/assets/fcc34444-6273-4e8f-9d64-4ff3f04115d5">

Enable PHP Features for OsTicket
 
Open IIS Manager:

- Bottom left type ISS and double click to run as admin
  
Navigate to the OsTicket Directory:

- In the Connections pane on the left, expand the Sites node.
- Click on the "Default Web Site" and then select the "osticket" folder.
  
Access PHP Manager:

- In the Actions pane on the right, click on "PHP Manager".

<br />
<img width="1336" alt="Screenshot 2024-09-20 at 1 34 26 PM" src="https://github.com/user-attachments/assets/b724515a-fca8-43ba-bb57-045e2b4c85b1">
<p>
</p>
<p>
</p>
<p> 
<img width="1332" alt="Screenshot 2024-09-20 at 1 39 24 PM" src="https://github.com/user-attachments/assets/632eacdd-2abe-43ce-a02a-e34205465818">
<p>
</p>
<p>
</p>
<p> 
 
Enable Necessary PHP Features:

- In the PHP Manager, you’ll see a list of PHP extensions and features that may not be enabled.

- Select the features that are currently disabled and enable them.

These are the three we will enable, double click them and click enable 
- Enable: php_imap.dll
- Enable: php_intl.dll
- Enable: php_opcache.dll

- After you enabled them please refresh OsTicket from the browser

<img width="1332" alt="Screenshot 2024-09-20 at 1 42 02 PM" src="https://github.com/user-attachments/assets/4dcc5555-280a-4069-9344-3465309ac10d">

Assign Permissions to the OsTicket Folder
Open File Explorer:

- Navigate to the File Explorer on your Windows virtual machine.
  
Access the wwwroot Folder:

- Go to the C:\inetpub\wwwroot directory where your web server files are stored.
  
Locate the OsTicket Folder:

- Find the "osticket" folder within the wwwroot directory.
- Click into the folder and find the file "include"

<img width="1143" alt="Screenshot 2024-09-20 at 1 58 34 PM" src="https://github.com/user-attachments/assets/4e6c3b46-2d1c-4e92-8abc-66692f60240e">

Rename the Configuration File

Locate the Sample Configuration File:

- Find the file named ost-sampleconfig.php within the include folder.
  
Rename the File:

- Right-click on ost-sampleconfig.php and select "Rename".
- Change the file name to ost-config.php and press Enter to continue.

  <img width="1115" alt="Screenshot 2024-09-20 at 2 02 01 PM" src="https://github.com/user-attachments/assets/d03b0e53-9d37-4806-bfea-d6e83ce397c5">

  <p>
</p>
<p>
</p>
<p> 
  
  

<img width="766" alt="Screenshot 2024-09-20 at 2 07 54 PM" src="https://github.com/user-attachments/assets/7709a0f8-e537-4eb9-b700-033526632419">
Allow osTicket to Modify Files in the Background

Open File Properties
- Access the File
- Double-click the newly renamed file or
- Right-click the file and select Properties from the context menu.
  
 Navigate to Security Settings
 
- Open the Security Tab:
- In the Properties window, click on the Security tab located at the top.

Access Advanced Security Settings
- Click on Advanced:
- Within the Security tab, click the Advanced button to open the Advanced Security Settings window.

Disable Inheritance
- Locate Disable Inheritance:
- In the Advanced Security Settings window, find the Disable inheritance option at the bottom left.
Click Disable Inheritance:

Click Disable inheritance.
Choose How to Handle Inherited Permissions:


<img width="766" alt="Screenshot 2024-09-20 at 2 06 49 PM" src="https://github.com/user-attachments/assets/7d8ab1e6-5c7b-40b0-a754-dbeac837dde1">

  

Add New Permissions
- Click Add
- In the Advanced Security Settings window, click the Add button to create a new permission entry.
  
Select a Principal:

- Click Select a principal.
- Type "Everyone" in the box.
- Click Check Names to validate the entry.
- After click the box full control like below.

<img width="921" alt="Screenshot 2024-09-20 at 2 20 45 PM" src="https://github.com/user-attachments/assets/10a3e056-2335-4512-99a6-4a7961567c9e">

 <p>
</p>
<p>
</p>
<p> 
<img width="914" alt="Screenshot 2024-09-20 at 2 25 09 PM" src="https://github.com/user-attachments/assets/f192de94-82df-45df-b568-d842c0269186">
  <p>
</p>
<p>
</p>
<p> 
- Everything should look like hte image below. Please click "apply" then ok.
<img width="767" alt="Screenshot 2024-09-20 at 2 26 07 PM" src="https://github.com/user-attachments/assets/01090ac9-f46d-409e-ad72-ba100d4ab352">
  <p>
</p>
<p>
</p>
<p> 
 Click ok for this window
   
 <img width="360" alt="Screenshot 2024-09-20 at 2 27 24 PM" src="https://github.com/user-attachments/assets/a81cfde8-7dcf-4729-b2e7-106c4d21ec96">

Finish Installation and Sign Up in osTicket Browser

Open Your Web Browser:
- Navigate to the osTicket installation URL.
  
Fill Out the Installation Form:

- Complete all required fields in the sign-up form.
- Ensure that all email addresses used are different to avoid any conflicts or issues.
  
Record Admin Credentials:

- Write down the username and password you create for the admin account.
- Keep this information secure, as it is essential for accessing the admin panel.
 
<img width="1165" alt="Screenshot 2024-09-20 at 2 33 27 PM" src="https://github.com/user-attachments/assets/82b0d398-c582-4112-a227-aad175651ff7">
Fixing the Database Section

Install HeidiSQL
- Locate HeidiSQL Installer:
- Within the osTicket installation folder, find the HeidiSQL installer file.

Run the Installer:

- Double-click the HeidiSQL installer to start the installation process.
  
Follow Installation Prompts:

- Accept the license agreement when prompted.
- Click Next on the subsequent windows to proceed through the installation steps.
- Choose the installation directory if prompted, or proceed with the default settings.
- Click Install to begin the installation.
- Once installation is complete, click Finish.

<img width="1136" alt="Screenshot 2024-09-20 at 2 42 53 PM" src="https://github.com/user-attachments/assets/d5351b94-570f-4faf-85b3-436d9bc05134">

 <p>
</p>
<p>
</p>
<p> 
 
<img width="592" alt="Screenshot 2024-09-20 at 2 45 11 PM" src="https://github.com/user-attachments/assets/0ea8fef5-5df8-4762-be24-563b0f5cdbb4">
- Skip this window
<img width="384" alt="Screenshot 2024-09-20 at 2 47 01 PM" src="https://github.com/user-attachments/assets/9ff172dc-ea29-4277-b893-26924cde1d78">

 Establish a Database Connection in HeidiSQL
Click "New":

- In the currently opened HeidiSQL window, click the "New" button located in the lower left corner.
  
Fill in Credentials:

- Username: Ensure it is set to root.
- Password: Enter the password associated with the root user.
  
Click "Open":

- After entering the credentials, click the "Open" button to establish the connection.

<img width="677" alt="Screenshot 2024-09-20 at 2 50 30 PM" src="https://github.com/user-attachments/assets/3634af5a-45de-4544-ac73-4d05aac037ca">

Create a Database in HeidiSQL for osTicket

Click "Unnamed":
- In the top right corner of the HeidiSQL window, click on "Unnamed".
  
Create a New Database:
- Select "Create new", then choose "Database".
  
Name the Database:
- Enter "osTicket" as the database name.
  
Confirm Creation:
- Click "OK" to create the database.

<img width="934" alt="Screenshot 2024-09-20 at 2 56 32 PM" src="https://github.com/user-attachments/assets/f90948c4-47ed-43ff-8f65-5f8591e83c4b">
<p>
</p>
<p>
</p>
<p> 
<img width="925" alt="Screenshot 2024-09-20 at 2 58 10 PM" src="https://github.com/user-attachments/assets/4404c602-e48d-497d-a5c0-9be46ab48c9a">

We will now head back to osTicket browser and please fill out the bottom form as shown in the screenshot. Username and password is root and click install now

<img width="1243" alt="Screenshot 2024-09-20 at 3 13 57 PM" src="https://github.com/user-attachments/assets/f28f1273-6144-4f24-a334-91a0f9d3e60e">

Congrats you have successfully instaleld osTicket. Your window should look like this.

<img width="820" alt="Screenshot 2024-09-20 at 3 15 03 PM" src="https://github.com/user-attachments/assets/24791ecd-7e30-4164-91a9-4db7e39c2d52">


