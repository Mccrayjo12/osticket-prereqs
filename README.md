<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

1. Azure account with permissions to create virtual machines
2. Remote Desktop Protocol (RDP) client for accessing the VM
3. osTicket installation files
4. Internet Information Services (IIS) enabled with CGI
5. MySQL database server and PHP extensions for IIS

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Begin by creating an Azure Virtual Machine with the following specifications: Name: osticket-vm, OS: Windows 10 (21H2), and vCPUs: 4. Use Remote Desktop to log into the VM with the provided credentials (labuser and osTicketPassword1!). Once in the VM, download the osTicket-Installation-Files.zip and unzip it onto the desktop. To enable IIS on the VM, go to Control Panel > Programs and Features > Turn Windows features on or off, and select IIS along with CGI under Application Development Features.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, proceed with the installation of PHP components and MySQL. From the osTicket-Installation-Files folder, install PHP Manager for IIS and the Rewrite Module. Create a directory at C:\PHP and unzip PHP 7.3.8 into this folder. Install the required Microsoft Visual C++ Redistributable (VC_redist.x86.exe) and then MySQL 5.5.62 using the “Typical Setup” configuration. After installation, launch the MySQL Configuration Wizard, set up with Username: root, Password: root, and choose Standard Configuration.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once these prerequisites are in place, configure IIS and complete the osTicket setup. In IIS Manager, use PHP Manager to register PHP by selecting the php-cgi.exe file in C:\PHP, and restart IIS. Copy the upload folder from osTicket-Installation-Files into C:\inetpub\wwwroot and rename it to osTicket. In IIS, enable the PHP extensions php_imap.dll, php_intl.dll, and php_opcache.dll. Rename ost-sampleconfig.php to ost-config.php, set permissions, and configure the database with HeidiSQL by creating an osTicket database. Finalize the setup by filling in the database information in the browser and completing the osTicket installation.
</p>
<br />
