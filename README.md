<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation using Azure</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure: Hosting the virtual machine (VM).
- Remote Desktop (RDP): Managing the VM.
- Internet Information Services (IIS): Web server for hosting osTicket.
- PHP 7.3.8: Required for osTicket to run.
- MySQL 5.5.62: Database for storing osTicket data.
- HeidiSQL: Database management tool.

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

**1. Microsoft Azure Virtual Machine**

- Purpose: Host the Windows environment for osTicket.
- Setup: Provision a VM with Windows 10 (21H2) or a compatible server OS.

**2. Internet Information Services (IIS)**

- Purpose: Host the osTicket web application.
- Setup: Enable IIS with CGI and HTTP features.

**3. PHP 7.3.8 (NTS)**

- Purpose: Execute PHP scripts required by osTicket.
- Setup: Install PHP in C:\PHP and register it with IIS using PHP Manager.

**4. URL Rewrite Module for IIS**

- Purpose: Enable clean and functional URLs in osTicket.

**5. Microsoft Visual C++ Redistributable**

- Purpose: Provide runtime support for PHP.

**6. MySQL Server 5.5.62**

Purpose: Database server to store osTicket data.

**7. HeidiSQL**

Purpose: Manage MySQL databases.

<h2>Installation Steps</h2>

**1. Install osTicket v1.15.8**
- Unzip osTicket-v1.15.8.zip from the installation files.
- Copy the upload folder to C:\inetpub\wwwroot.
- Rename upload to osTicket.
  
**2. Configure IIS**
- Reload IIS:
- Open IIS.
- Stop and Start the server.
- Go to Sites > Default > osTicket.
- On the right, click “Browse *:80” to open osTicket in your browser.
  
**3. Enable PHP Extensions**
- In IIS, go to Sites > Default > osTicket.
- Double-click PHP Manager.
- Click “Enable or disable an extension” and enable:
- php_imap.dll
- php_intl.dll
- php_opcache.dll
  
**4. Configure ost-config.php**
- Rename the file:
- From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
- To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
- Assign permissions:
- Disable inheritance and remove all permissions.
- Add Everyone with Full Control.
  
**5. Set Up the Database**
- Install HeidiSQL from the installation files.
- Open HeidiSQL and create a new session (root/root).
- Connect to the session and create a database called osTicket.
  
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

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
