# osTicket - Prerequisites and Installation

This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.

## Environments and Technologies Used

- **Microsoft Azure (Virtual Machines/Compute)**
- **Remote Desktop**
- **Internet Information Services (IIS)**
- **Operating System:** Windows 10 (21H2)

## List of Prerequisites

- Azure Virtual Machine
- Internet Information Services (IIS)
- PHP Manager
- Rewrite Module
- VC Redist
- MySQL
- Heidi SQL
- osTicket v1.15.8

[Link to downloads](https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)

## Installation Steps

1. **Create a Virtual Machine:**
   - Go to [Azure portal](https://portal.azure.com/).
   - Set up a virtual machine with Windows 10 Pro, version 22H2, with at least 2 vCPUs and 16GBs of memory.

2. **Connect to the Virtual Machine:**
   - Connect using Remote Desktop Connection app using the public IP address of the VM.

3. **Enable Internet Information Services (IIS) in Windows:**
   - Go to Control Panel -> Programs -> Turn Windows features on and off.
   - Install/enable IIS with CGI and Common HTTP Features.

4. **Install PHP Manager for IIS:**
   - Download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi).

5. **Install Rewrite Module:**
   - Download and install the Rewrite Module (rewrite_amd64_en-US.msi).

6. **Install PHP:**
   - Create a folder named `PHP` in the C drive.
   - Download PHP 7.3.8 (php-7.3.88-nts-Win32-VC15-x866.zip) and unzip it into `C:\PHP`.
   - Download and install VC_redist.x86.exe from the installation files.

7. **Install MySQL:**
   - Download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi).
   - Set up MySQL with a root password (e.g., Password1).

8. **Register PHP in IIS:**
   - Open IIS as an administrator.
   - Click on PHP Manager and register new PHP version by providing the path to `php-cgi.exe` in `C:\PHP`.

9. **Install osTicket:**
   - Download osTicket from the Installation Files Folder.
   - Extract and copy the "upload" folder to `C:\inetpub\wwwroot`.
   - Rename the "upload" folder to "osTicket".
   - Reload IIS.

10. **Enable PHP Extensions:**
    - Go to sites -> Default -> osTicket in IIS.
    - Enable the following PHP extensions in PHP Manager: 
      - php_imap.dll
      - php_intl.dll
      - php_opcache.dll

11. **Configure osTicket:**
    - Rename `ost-sampleconfig.php` to `ost-config.php`.
    - Set appropriate permissions for `ost-config.php`.
    - Continue the setup in the browser, providing necessary information except for the Database Settings.

12. **Install HeidiSQL:**
    - Download and install HeidiSQL from the Installation Files.
    - Create a new session with root username and Password1.

13. **Create Database:**
    - Create a new database named `osTicket` in HeidiSQL.
    - Provide the same database name (`osTicket`) in osTicket setup.

14. **Clean Up:**
    - Delete the `setup` folder from `C:\inetpub\wwwroot\osTicket`.
    - Set permissions of `ost-config.php` to "Read" only.

15. **Finish Setup:**
    - Login to osTicket in the browser.

Congratulations! You have now successfully installed and setup osTicket!





osTicket - Prerequisites and Installation

This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.

Environments and Technologies Used
Microsoft Azure (Virtual Machines/Compute)
Remote Desktop
Internet Information Services (IIS)
Operating Systems Used
Windows 10 (21H2)
List of Prerequisites
Azure Virtual Machine
Internet Information Services (IIS)
PHP Manager
Rewrite Module
VC Redist
MySQL
Heidi SQL
osTicket v1.15.8
Link to downloads: https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6
Installation Steps
1.) The first thing you are going to want to do is create a virtual machine by going to https://portal.azure.com/. Setup your virtual machine with Windows 10 Pro, version 22H2. Note, you will want to create a virtual machine with atleast 2 vcpus and 16 gbs of memory.

2.) Once you have created your virtual machine you will want to conncet to it by using the public ip address the vm is setup with. You will connect using the remote desktop connection app.

Disk Sanitization Steps

Disk Sanitization Steps

3.) Once you have connected to your virtual machine you will want to go to your control panel. From the control panel open up programs. Select, Turn Windows features on and off.

Disk Sanitization Steps

Disk Sanitization Steps

4.) You will want to install / enable IIS in Windows with CGI and Common HTTP Features

World Wide Web Services -> Application Development Features -> [X] CGI [X] Common HTTP Features
Disk Sanitization Steps

Disk Sanitization Steps

NOTE Make sure all Common HTTP Features are checked.

To make sure the IIS is installed / enabled go to a browser of your choice and search for 127.0.0.1 It should look something like this.

Disk Sanitization Steps

5.) Now that the IIS is enabled, From the Installation Files, download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) Go through the install wizard and complete the install.

6.) Next from the Installation Files, download and install the Rewrite Module (rewrite_amd64_en-US.msi)

7.) Create a folder in the C drive called PHP.

8.) From the Installation Files, download PHP 7.3.8 (php-7.3.88-nts-Win32-VC15-x866.zip) and unzip the contents into C:\PHP

!! ATTENTION !! If this appears, choose to “Keep” the file:

Disk Sanitization Steps

Disk Sanitization Steps

9.) Once you have downloaded and extracted the zip file into the PHP folder on the C drive, download and install the VC_redist.x86.exe from the installation files. Go through the setup wizard to finish setting up and installing the VC_redist.x86.exe.

10.) Download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi) Run the setup wizard: Typical Setup -> Launch Configuration Wizard (after install) -> Standard Configuration ->

Make the new root password: Password1

Disk Sanitization Steps

Execute the process on the next page.

Disk Sanitization Steps

11.) Now that we have the files downloaded and installed we will want to search for IIS in the windows search bar. Open IIS as an administrator. The program should look like this.

Disk Sanitization Steps

12.) We will now want to register PHP from within IIS. Click on PHP Manager

Disk Sanitization Steps

Register new PHP version.

Disk Sanitization Steps

You will want to provide a path to the php executable file (php-cgi.exe)). Go to C Drive -> PHP -> click on php-cgi file.

Disk Sanitization Steps

Restart the IIS server.

Disk Sanitization Steps

13.) Install osTicket v1.15.8 -Download osTicket from the Installation Files Folder -Extract and copy "upload" folder to c:\inetpub\wwwroot -Within c:\inetpub\root, Rename "upload" to "osTicket"

Reload IIS again.

14.) On IIS go to sites -> Default -> osTicket -On the right, click “Browse *:80”

Disk Sanitization Steps

Some extensions are not enabled on the osTicket browser.

Disk Sanitization Steps

To enable the extensions: -Go back to IIS, sites -> Default -> osTicket -Double click PHP manager -Click "Enable or disable an extension"

Disk Sanitization Steps

Disk Sanitization Steps

We will want to enable three extensions from here.

1.) php_imap.dll

2.) php_intl.dll

3.) php_opcache.dll

Disk Sanitization Steps

15.) Once we have those extensions enabled in IIS, we are going to want to rename one of the files in our osTicket folder. Go into the file explorer and search for C;\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php

We are going to rename the ost-sampleconfig.php to ost-config.php

Now that we have renamed the files, right click on the file and go to properties. From there click security, click on advance, and disable the inheritance. We will select Remove all inherited permissions from this object.

Now we will add new permissions.

Click Add

Disk Sanitization Steps

Select a principal

Disk Sanitization Steps

Type "Everyone" in the box.

Disk Sanitization Steps

Make sure Full Control and all the other boxes are checked.

Disk Sanitization Steps

Click Apply and Ok.

Disk Sanitization Steps

Once that is done we will continue to setup osTicket in the browser. Click Continue on the osTicket browser page. Fill out the page as required except the Database Settings at the bottom of the page. We will get to that.

We will want to download and install HeidiSQL from the Installation Files.

Disk Sanitization Steps

When the program is open we will create a new session in it.

Disk Sanitization Steps

We want to make sure the username is root and the password is Password1.

Disk Sanitization Steps

Once we are connected to the session we will go back to the browser to finish setting everything up. Under the Database Settings in the browser the username will be root and the password will be Password1.

We will now create a new database within HeidiSQL. In Heidi right click on the left side where is says "Unnamed", select "create new", and then select "database". Name the new database osTicket. Once we have the new database setup go back to the osTicket browser and under MySQL Database type in osTicket.

Disk Sanitization Steps

The last step is to do some clean up. We will want to delete the setup folder in our system. -Delete: C:\inetpub\wwwroot\osTicket\setup Only delete the setup folder and nothing else.

We then will want to set the permissions back to "Read" only in the ost-config.php file.

Disk Sanitization Steps

Disk Sanitization Steps

The last step after that is to login to osTicket on the browser.

Disk Sanitization Steps

Congrats! You have now successfully installed and setup osTicket!

