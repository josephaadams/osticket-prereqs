<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure: Hosting the virtual machine 
- Remote Desktop: Accessing and managing the VM
- Internet Information Services (IIS): Web server for hosting osTicket
- Operating System: Windows 10 

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- **Microsoft Azure Virtual Machine**

Purpose: Hosts the Windows environment where osTicket will be installed.

Setup: Provision a VM with Windows 10 (21H2), ensuring adequate resources (e.g., 2 CPUs, 4GB RAM).

- **Remote Desktop Connection (RDP)**

Purpose: Allows remote access to the Azure VM for configuration and management.

Setup: Use the Remote Desktop client to connect to the VM using its public IP address.

- **Internet Information Services (IIS)**

Purpose: Serves as the web server to host the osTicket application.

Setup: Enable IIS on the VM:
Navigate to Control Panel > Programs > Turn Windows features on or off.
Expand Internet Information Services > World Wide Web Services > Application Development Features.
Check CGI.
Ensure Common HTTP Features are also enabled.

- **PHP Manager for IIS**

Purpose: Simplifies the management of PHP installations and configurations within IIS.

Setup: Install PHP Manager for IIS from the official source or included installation files.

- **URL Rewrite Module for IIS**

Purpose: Enables URL rewriting capabilities, allowing for cleaner and more user-friendly URLs in osTicket.

Setup: Install the URL Rewrite Module from Microsoft's official site or the provided installation files.

- **PHP 7.3.8 (Non-Thread Safe)**

Purpose: Executes the PHP scripts that power osTicket.

Setup:
Create a directory at C:\PHP.
Download and extract the PHP 7.3.8 NTS version into the C:\PHP folder.
Register PHP within IIS using PHP Manager, pointing to C:\PHP\php-cgi.exe.

- **Microsoft Visual C++ Redistributable (VC_redist.x86.exe)**

Purpose: Provides necessary runtime components required by PHP to function correctly.

Setup: Install the Visual C++ Redistributable for Visual Studio 2015 (or the version corresponding to PHP 7.3.8) from Microsoft's official site or the provided installation files.

- **MySQL Server 5.5.62**

Purpose: Serves as the database management system to store osTicket data, including tickets, user information, and configurations.

Setup:
Download and install MySQL Server 5.5.62.
During installation, set a root password and configure the server as per your requirements.
After installation, create a database named osticket for the application.

- **osTicket Installation Files**

Purpose: Contains the core files necessary to install and run osTicket.

Setup:
Download the osTicket installation package.
Extract the contents and copy the upload folder to C:\inetpub\wwwroot.
Rename the upload folder to osTicket.
Ensure the C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php file is renamed to ost-config.php.
Adjust file permissions to allow IIS to write to the configuration file during setup.

<h2>Installation Steps</h2>

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
