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

- Windows 10</b> (22H2)

<h2>List of Prerequisites</h2>

- Enable IIS
- Install Web Platform Installer
- Install MySQL and setup username and password
- Install Microsoft Visual C++ 2009 Redistributable Package
- Configure permissions and install osTicket

<h2>Installation Steps</h2>

<p>
<img src="https://github.com/user-attachments/assets/930058c7-5382-4724-8e53-0f2ccdc4be19" height="50%" width="50%"/>
</p>
<p>
You'll be starting this project on a Virtual Machine using Microsoft Azure. We will be using Windows 10 Pro (22H2).
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/2407cdcc-006d-46ea-8256-5c1b5e1dea73" height="50%" width="50%"/>
</p>
<p>
We are now going to connect to our Virtual Machine. Open Remote Desktop Connection and paste the VM's public IP. The public IP can be found in the Azure portal when you view the details of the VM you created. Enter the administrator credentials you created to sign in.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/2407cdcc-006d-46ea-8256-5c1b5e1dea73" height="50%" width="50%"/>
</p>
<p>
We are now going to connect to our Virtual Machine. Open Remote Desktop Connection and paste the VM's public IP. The public IP can be found in the Azure portal when you view the details of the VM you created. Enter the administrator credentials you created to sign in.
</p>
<br />

<p>
<img src="https://i.imgur.com/UabnZWy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once you've got Windows 10 open, head over to the Control Panel and click "Uninstall a program" underneath Program. On the left you'll see "Turn Windows features on or off". Click this and the window above will pop up. Select "Internet Information Services" (ISS) and click okay.
</p>
<br />

<p>
<img src="https://i.imgur.com/yvSCCFY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download and install Microsoft Web Platform 5.1
</p>
<br />

<p>
<img src="https://i.imgur.com/keL1rqQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Launch Microsoft Web Platform 5.1 and add MySQL Windows 5.5
</p>
<br />

<p>
<img src="https://i.imgur.com/eflBy4u.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, search for "php" and sort the list to make it easier to select the necessary versions. Add PHP 5.6.31, 7.0.33(x86), 7.1.29(x86), 7.2.26(x86), and 7.3.25(x86). There should be 12 items to install. Click install.
</p>
<br />

<p>
<img src="https://i.imgur.com/6EPvb2g.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
You'll be asked to create a password for MySQL. The user will be "root". Write down the password twice and don't forget it. Click continue.
</p>
<br />

<p>
<img src="https://i.imgur.com/R4wJ7kx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once the installation completes, you'll notice a few things failed and that's okay. We will install those next.
</p>
<br />

<p>
<img src="https://i.imgur.com/f1hrbm4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download Microsoft Visual C++ 2008 (vcredist_x86) and PHPManagerForIIS_V1.5.0
</p>
<br />

<p>
<img src="https://i.imgur.com/0OjBqdd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install Microsoft Visual C++ 2008 (vcredist_x86)
</p>
<br />

<p>
<img src="https://i.imgur.com/cScpfpK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install PHP Manager
</p>
<br />

<p>
<img src="https://i.imgur.com/UwohvaB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download and extract osTicket-v1.15.8
</p>
<br />

<p>
<img src="https://i.imgur.com/gUWmgob.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After extracting, copy the upload folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/9txh0gn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Paste the "upload" folder to This PC > Windows (C:) > inetpub > wwwroot
</p>
<br />

<p>
<img src="https://i.imgur.com/I0plZ7r.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Rename the "upload" folder to "osTicket"
</p>
<br />

<p>
<img src="https://i.imgur.com/4QTkNsN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open up IIS. You can search for it in the search bar on the bottom left. On the right side of the window, click "restart".
</p>
<br />

<p>
<img src="https://i.imgur.com/sukJyCD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
On the left, open the drop down vm-osticket > Sites > Default Web Site > osTicket. Select osTicket and on the right side of the window, click "Browse *:80 (http)"
</p>
<br />

<p>
<img src="https://i.imgur.com/wAxRd3Y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The browser should open with osTicket Installer.
</p>
<br />

<p>
<img src="https://i.imgur.com/pppgQJg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open IIS Manager again and click PHP Manager. 
</p>
<br />

<p>
<img src="https://i.imgur.com/R1XjNgm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Click "Enable or disable an extension" on the bottom
</p>
<br />

<p>
<img src="https://i.imgur.com/PnZspmr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Right click and enable php_intl.dll
</p>
<br />

<p>
<img src="https://i.imgur.com/LVkAqRc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Make sure php_imap.dll is enabled.
</p>
<br />

<p>
<img src="https://i.imgur.com/IXS4Jur.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Enable php_opcache.dll
</p>
<br />

<p>
<img src="https://i.imgur.com/OLzDJaI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Refresh the browser and observe the changes.
</p>
<br />

<p>
<img src="https://i.imgur.com/FWhCE11.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Changes made.
</p>
<br />

<p>
<img src="https://i.imgur.com/wLLoqqX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Navigate to the folder: This PC > Windows (C:) > inetpub › wwwroot > oslicket > include. Find and rename "ost-sampleconfig.php" to "ost-config.php". Make sure the spelling is correct.
</p>
<br />

<p>
<img src="https://i.imgur.com/Nn7vMdT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Disable the inheritance of the ost-config.php file.
</p>
<br />

<p>
<img src="https://i.imgur.com/YbB6lUu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Select principal and allow "Everyone".
</p>
<br />

<p>
<img src="https://i.imgur.com/tYIJfz1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Allow all permissions.
</p>
<br />

<p>
<img src="https://i.imgur.com/80cvh5d.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Click continue on osTicket and you'll see "osTicket Basic Installation".
</p>
<br />

<p>
<img src="https://i.imgur.com/afuxNZq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download and install HeidiSQL 12.0.0.6468.
</p>
<br />

<p>
<img src="https://i.imgur.com/TbQhVHy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a new connection and use the password you created with MySQL. Remember the user was "root". Click open.
</p>
<br />

<p>
<img src="https://i.imgur.com/3S7arYq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now create a new database.
</p>
<br />

<p>
<img src="https://i.imgur.com/PApnB6Y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I went ahead and named it osTicket to keep things simple.
</p>
<br />

<p>
<img src="https://i.imgur.com/B5rSP4i.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Navigate back to the browser and osTicket Basic Installation and input the database name, root user, and the password created with MySQL.
</p>
<br />

<p>
<img src="https://i.imgur.com/PlrJTKz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Click Install to finish the process.
</p>
<br />

<p>
<img src="https://i.imgur.com/0f9jJxM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now let's navigate back to delete the setup folder, otherwise osTicket will bug you with alerts to setup.
</p>
<br />

<p>
<img src="https://i.imgur.com/8zN97BO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Delete the contents of the setup folder to be able to delete the actual folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/aySy4LW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Navigate back to the ost-config.php file and change its permissions to "Read and execute" and "Read". Don't forget to apply the changes before hitting okay.
</p>
<br />

<p>
<img src="https://i.imgur.com/Gm7YVUv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Head back to the browser with osTicket and open a new tab with the link underneath "Your Staff Control Panel".
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/29f0d4d0-9459-4cbd-a175-4ebe16cca20d" height="80%" width="80%"/>
</p>
<p>
Login with the username and password you chose during the installation of osTicket.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/e780d00c-06b2-4fb7-ad9c-86cce90a520a" height="60%" width="60%"/>
</p>
<p>
This is how the application should look like after initial log in. Congratulations on installing osTicket!
</p>
<br />



































































