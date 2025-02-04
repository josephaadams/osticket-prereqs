<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation using Azure</h1>
This project demonstrates the steps to set up and install osTicket v1.15.8 on a Windows server environment. The guide includes configuring the necessary prerequisites, installing osTicket, and setting up the database.<br />


<h2>Download Required Files</h2>

**All necessary installation files can be downloaded from the link below:** 

### [Download Installation Files](https://drive.google.com/file/d/1jp6LjByxja6CpoSbOz6Cs8BUIdk_gbSx/view?usp=drive_link)



<h2>Environments and Technologies Used</h2>

- Microsoft Azure: Hosting the virtual machine.
- Remote Desktop (RDP): Managing the VM.
- Internet Information Services (IIS): Web server for hosting osTicket.
- PHP 7.3.8: Required for osTicket to run.
- MySQL 5.5.62: Database for storing osTicket data.
- HeidiSQL: Database management tool.

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Installation Steps</h2>

**1. Setup Microsoft Azure Virtual Machine** (If you need help creating a VM, follow my guide: https://github.com/josephaadams/azure-vmcreation

- Create a VM running Windows 10 (21H2) or a compatible server OS.

- Use Remote Desktop (RDP) to access the VM.

**2. Install Internet Information Services (IIS)** 

- Open Control Panel > Programs > Turn Windows features on or off.

- Check Internet Information Services (IIS) and enable CGI and HTTP features

**3. Install PHP 7.3.8**

- Extract php-7.3.8-nts-Win32-VC15-x86.zip to C:\PHP.

- Register PHP with IIS using PHP Manager for IIS.

- Enable PHP Extensions:

. Open IIS Manager.

. Navigate to Sites > Default > osTicket.

. Double-click PHP Manager.

. Click "Enable or disable an extension" and enable:

. php_imap.dll

. php_intl.dll

. php_opcache.dll

**4. Install MySQL Server & HeidiSQL**
- Install MySQL Server (mysql-5.5.62-win32.msi).

- Set the root password to root.

- Install HeidiSQL (HeidiSQL_12.3.0.6589_Setup.exe).

**Create Database for osTicket:**

- Open HeidiSQL.

- Create a new session (root/root).

- Connect and create a database named osTicket.

<img src="https://i.imgur.com/tlwie81.png"/>

**5. Install osTicket v1.15.8**
- Unzip osTicket-v1.15.8.zip from the installation files.
- Copy the upload folder to C:\inetpub\wwwroot.
- Rename upload to osTicket.

<img src="https://i.imgur.com/yxkKp2E.png"/>
  
**6. Configure IIS for osTicket**
- Open IIS Manager
- Stop and Start the server.
- Go to Sites > Default > osTicket.
- On the right panel, click “Browse *:80” to open osTicket in your browser.

<img src="https://i.imgur.com/06iSCbJ.png"/>

**3. Enable PHP Extensions** (REMOVE STEP)
- In IIS, go to Sites > Default > osTicket.
- Double-click PHP Manager.
- Click “Enable or disable an extension” and enable:
- php_imap.dll
- php_intl.dll
- php_opcache.dll

<img src="https://i.imgur.com/qKDXNtr.png"/>
  
**7. Configure ost-config.php**
- Rename the file:
- From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
- To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
- Assign permissions:
- Right-click ost-config.php > Properties.
- Click Security > Advanced.
- Disable inheritance and remove all permissions.
- Add Everyone with Full Control.

  <img src="https://i.imgur.com/N63QY76.png"/>

**8. Complete osTicket Setup in the Browser**
- Open the osTicket installation page in your browser.
- Enter the following details:
- Helpdesk Name: Choose a name for your help desk.
- Default Email: Specify an email address to receive customer tickets.
- MySQL Database: osTicket
- MySQL Username: root
- MySQL Password: root
- Click Install Now!


<p>
<img src="https://i.imgur.com/5TZ1qmz.png"/>
</p>
<p>
Congratulations! You have successfully installed osTicket on your server. If you have any questions, refer to the official osTicket documentation https://docs.osticket.com/en/latest/
</p>
<br />


