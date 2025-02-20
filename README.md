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

- 1. Web Server
Apache or Nginx: osTicket requires a web server to serve its pages. Apache is the most common choice, but Nginx can also be used with some adjustments.

- 2. PHP Version
PHP 7.4 or later (recommended PHP 8.0 or later)
Ensure PHP is installed and properly configured on your server.
osTicket uses several PHP extensions, so make sure these are enabled (see below).

- 3. PHP Extensions
You will need to install and enable the following PHP extensions:

PHP MySQLi
PHP GD (for image manipulation)
PHP IMAP (for email integration)
PHP JSON (for handling JSON data)
PHP Mbstring (for multi-byte string handling)
PHP cURL (optional, for email and ticket system integrations)

- 4. Database Server
MySQL (version 5.5 or later) or MariaDB
You’ll need a MySQL/MariaDB database to store all your ticketing data.
Create a database and user before installing osTicket.

- 5. File Permissions
You’ll need to ensure proper file permissions for the osTicket directories, especially for directories like:
include/
attachments/
uploads/
admin/
These directories must be writable by the web server.

- 6. Operating System
osTicket can be installed on any Unix-based OS (Linux, Ubuntu, CentOS) or Windows. A Linux server is often the most recommended setup.

- 7. Email Configuration (optional but recommended)
If you plan to integrate email support (such as ticket creation via email), you will need:
SMTP server information for outgoing emails.
IMAP or POP3 server information for fetching emails.

<h2>Installation Steps</h2>

<p>
Download osTicket:
Visit the official osTicket website and download the latest stable version.

Unzip & Place Files:
Unzip the osTicket files and upload them to your server, typically in the public_html or www directory of your web server.
</p>
<br />

<p>
<img src="https://i.imgur.com/boaNJwx.png"/>
</p>
<p>
Within the VM (osticket-vm), download the osTicket-Installation-Files.zip and unzip it onto your desktop. The folder should be called “osTicket-Installation-Files”
We will use the files in this folder to install osTicket and some of the dependencies.

</p>
<br />

<p>
<img src="https://i.imgur.com/nThtG7R.jpeg"/>
</p>
<p>
Install / Enable IIS in Windows WITH CGI
World Wide Web Services -> Application Development Features -> [X] CGI

From the “osTicket-Installation-Files” folder, install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)

From the “osTicket-Installation-Files” folder install the Rewrite Module (rewrite_amd64_en-US.msi)

Create the directory C:\PHP

From the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder

From the “osTicket-Installation-Files” folder, install VC_redist.x86.exe.

From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
Typical Setup ->
Launch Configuration Wizard (after install) ->
Standard Configuration ->
Username: root
Password: root

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
