<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation using Azure</h1>
This project demonstrates the steps to set up and install osTicket v1.15.8 on a Windows server environment. The guide includes configuring the necessary prerequisites, installing osTicket, and setting up the database.<br />


<h2>Files Needed</h2>

**Download the required files from the link below. These files include all necessary installers and packages for setting up osTicket.** 

### [Download Installation Files](https://drive.google.com/file/d/1jp6LjByxja6CpoSbOz6Cs8BUIdk_gbSx/view?usp=drive_link)


Included Files:

1. Rewrite Module for IIS (rewrite_amd64_en-US.msi)
- Required for URL rewriting in IIS.

2. Microsoft Visual C++ Redistributable (VC_redist.x86.exe)
- Provides runtime libraries required by PHP.

3. osTicket v1.15.8 (osTicket-v1.15.8.zip)
- Contains the osTicket application files.

4. PHP 7.3.8 (NTS) (php-7.3.8-nts-Win32-VC15-x86.zip)
- PHP runtime required for osTicket.

5. PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
- Tool to manage PHP configurations in IIS.

6. MySQL Server (mysql-5.5.62-win32.msi)
- Database server to store osTicket data.

7. HeidiSQL (HeidiSQL_12.3.0.6589_Setup.exe)
- Database management tool for MySQL.


<h2>Environments and Technologies Used</h2>

- Microsoft Azure: Hosting the virtual machine.
- Remote Desktop (RDP): Managing the VM.
- Internet Information Services (IIS): Web server for hosting osTicket.
- PHP 7.3.8: Required for osTicket to run.
- MySQL 5.5.62: Database for storing osTicket data.
- HeidiSQL: Database management tool.

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

**1. Microsoft Azure Virtual Machine** (If you don't know how to create a VM using azure, check out my guide: **********REPLACEEEEE**********)

- Purpose: Host the Windows environment for osTicket.
- Setup: Provision a VM with Windows 10 (21H2) or a compatible server OS.

**2. Internet Information Services (IIS)** 

- Purpose: Host the osTicket web application.
- Setup: Enable IIS with CGI and HTTP features.

**3. PHP 7.3.8 (NTS)** (Included in the Installation Files)

- Purpose: Execute PHP scripts required by osTicket.
- Setup: Install PHP in C:\PHP and register it with IIS using PHP Manager.

**4. URL Rewrite Module for IIS** (Included in the Installation Files)

- Purpose: Enable clean and functional URLs in osTicket.

**5. Microsoft Visual C++ Redistributable** (Included in the Installation Files)

- Purpose: Provide runtime support for PHP.

**6. MySQL Server 5.5.62** (Included in the Installation Files)

Purpose: Database server to store osTicket data.

**7. HeidiSQL** (Included in the Installation Files)

Purpose: Manage MySQL databases.

<h2>Installation Steps</h2>

**1. Install osTicket v1.15.8**
- Unzip osTicket-v1.15.8.zip from the installation files.
- Copy the upload folder to C:\inetpub\wwwroot.
- Rename upload to osTicket.

<img src="https://i.imgur.com/yxkKp2E.png"/>
  
**2. Configure IIS**
- Reload IIS:
- Open IIS.
- Stop and Start the server.
- Go to Sites > Default > osTicket.
- On the right, click “Browse *:80” to open osTicket in your browser.

<img src="https://i.imgur.com/06iSCbJ.png"/>

**3. Enable PHP Extensions**
- In IIS, go to Sites > Default > osTicket.
- Double-click PHP Manager.
- Click “Enable or disable an extension” and enable:
- php_imap.dll
- php_intl.dll
- php_opcache.dll

<img src="https://i.imgur.com/qKDXNtr.png"/>
  
**4. Configure ost-config.php**
- Rename the file:
- From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
- To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
- Assign permissions:
- Disable inheritance and remove all permissions.
- Add Everyone with Full Control.

  <img src="https://i.imgur.com/N63QY76.png"/>
  
**5. Set Up the Database**
- Install HeidiSQL from the installation files.
- Open HeidiSQL and create a new session (root/root).
- Connect to the session and create a database called osTicket.

<img src="https://i.imgur.com/tlwie81.png"/>
  
**6. Complete osTicket Setup in the Browser**
- Open the osTicket installation page in your browser.
- Provide the following details:
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
Congratulations on the installation of osTicket on your server! If you have any questions please make sure to check out osTickets docs https://docs.osticket.com/en/latest/
</p>
<br />


