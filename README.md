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

https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6

## Installation Steps

1. **Create a Virtual Machine:**
   - Go to [Azure portal](https://portal.azure.com/).
   - Set up a virtual machine with Windows 10 Pro, version 22H2, with at least 2 vCPUs and 16GBs of memory.
 <img width="501" alt="step 1A" src="https://github.com/AlexisVal08/ostickets-prereqs/assets/135868956/cedf7be0-f9f5-49c9-92e4-8e00348af09d">
 <img width="504" alt="step 2B" src="https://github.com/AlexisVal08/ostickets-prereqs/assets/135868956/84dc9a15-aba5-46a4-a10c-20d61bd7b4ca">


2. **Connect to the Virtual Machine:**
   - Connect using Remote Desktop Connection app using the public IP address of the VM.
   - Also using the assigned login account and password
<img width="428" alt="step 2A" src="https://github.com/AlexisVal08/ostickets-prereqs/assets/135868956/7d287a6f-7662-44b8-aa66-bd0dfd0860b3">
<img width="427" alt="step 2B" src="https://github.com/AlexisVal08/ostickets-prereqs/assets/135868956/2ee2d001-afe3-4eae-ab2c-c1723323dcb2">


3. **Enable Internet Information Services (IIS) in Windows:**
   - Go to Control Panel -> Programs -> Turn Windows features on and off.
   - Install/enable IIS with CGI and Common HTTP Features
   - World Wide Web Services -> Application Development Features
<img width="428" alt="Step 3A" src="https://github.com/AlexisVal08/ostickets-prereqs/assets/135868956/3500648f-1918-4e60-936c-b044af37cdfe">
<img width="428" alt="Step 3B" src="https://github.com/AlexisVal08/ostickets-prereqs/assets/135868956/f29a0296-6750-43a8-8c0d-a71d9b9f3a81">
<img width="260" alt="Step 3C" src="https://github.com/AlexisVal08/ostickets-prereqs/assets/135868956/dd056619-6198-4e04-99ec-053cbaf5656e">
<img width="260" alt="Step 3D" src="https://github.com/AlexisVal08/ostickets-prereqs/assets/135868956/efc7bad3-d3e9-4e8b-9bf5-49e01385753a">
<img width="260" alt="Step 3E" src="https://github.com/AlexisVal08/ostickets-prereqs/assets/135868956/fbc0c78a-a5ee-4f6a-8cfb-50c7513842f9">

4. **Install PHP Manager for IIS:**
   - Download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi).
<img width="428" alt="Step 4A" src="https://github.com/AlexisVal08/ostickets-prereqs/assets/135868956/2f7858ce-f605-4927-bb03-45289a4655ce">
<img width="428" alt="Step 4B" src="https://github.com/AlexisVal08/ostickets-prereqs/assets/135868956/7139fc0f-cc03-4422-bc58-b4ab9046b89f">

5. **Install Rewrite Module:**
   - Download and install the Rewrite Module (rewrite_amd64_en-US.msi).
<img width="428" alt="Step 5A" src="https://github.com/AlexisVal08/ostickets-prereqs/assets/135868956/4a0eb03a-391f-4b75-b285-7274c8ae611e">
<img width="428" alt="Step 5B" src="https://github.com/AlexisVal08/ostickets-prereqs/assets/135868956/5a7221b4-4115-4f55-a8ec-e52835b519d9">

6. **Install PHP:**
   - Create a Directory folder named `PHP` in the C drive.
   - Download PHP 7.3.8 (php-7.3.88-nts-Win32-VC15-x866.zip) extract and unzip it into `C:\PHP`.
   - Download and install VC_redist.x86.exe from the installation files.
<img width="428" alt="Step 6A" src="https://github.com/AlexisVal08/ostickets-prereqs/assets/135868956/58754f5b-074a-4e45-959b-50c831619b9e">
<img width="428" alt="Step 6B" src="https://github.com/AlexisVal08/ostickets-prereqs/assets/135868956/4bce4b49-c23f-4237-8d98-d678f5fa2bc9">
<img width="428" alt="Step 6C" src="https://github.com/AlexisVal08/ostickets-prereqs/assets/135868956/f8aa4c7d-1dbf-4227-8e7b-f46e7f52a199">
<img width="428" alt="Step 6D" src="https://github.com/AlexisVal08/ostickets-prereqs/assets/135868956/9f278f76-2369-4228-9aa9-1c10f1538f9a">
<img width="428" alt="Step 6E" src="https://github.com/AlexisVal08/ostickets-prereqs/assets/135868956/15f2e4af-36dd-4ad4-8fae-1c5cc05ed601">
<img width="428" alt="Step 6F" src="https://github.com/AlexisVal08/ostickets-prereqs/assets/135868956/c5310ff2-58e7-471c-9d37-f6bcec28f35e">
<img width="428" alt="Step 6G" src="https://github.com/AlexisVal08/ostickets-prereqs/assets/135868956/8f0a2578-8c83-4105-9802-666bb3b00528">


7. **Install MySQL:**
   - Download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi). For installation accept agreements and set my sql as typical. 
   - Set up MySQL with a root password (e.g., Password1).
   - MySQL server instance configuration wizard installation completion will create a database within the computer so it can storage occupied for osTicket.
<img width="428" alt="Step 7A" src="https://github.com/AlexisVal08/ostickets-prereqs/assets/135868956/b1298660-c6c7-4ee1-b377-bcb312ad32d9">
<img width="428" alt="Step 7B" src="https://github.com/AlexisVal08/ostickets-prereqs/assets/135868956/6eaf04e6-5bf5-458d-8e95-2b26e8913752">
<img width="428" alt="Step 7C" src="https://github.com/AlexisVal08/ostickets-prereqs/assets/135868956/dd86383b-381e-4bc9-845f-69638d06e68c">
<img width="428" alt="Step 7D" src="https://github.com/AlexisVal08/ostickets-prereqs/assets/135868956/940550ef-0a8c-444c-8987-328af44badc0">
<img width="428" alt="Step 7E" src="https://github.com/AlexisVal08/ostickets-prereqs/assets/135868956/52cec249-25c1-493c-acc3-b9a52eee2d20">

8. **Register PHP in IIS:**
   - Open IIS as an administrator.
   - Click on PHP Manager, register and enable the new PHP version by providing the path to `php-cgi.exe` in `C:\PHP`.
<img width="428" alt="Step 8A" src="https://github.com/AlexisVal08/ostickets-prereqs/assets/135868956/bf54eb39-d027-4a8b-87b5-19e9d5123331">
<img width="428" alt="Step 8B" src="https://github.com/AlexisVal08/ostickets-prereqs/assets/135868956/08074180-f5dc-4932-a107-fc19da2859b0">
<img width="428" alt="Step 8C" src="https://github.com/AlexisVal08/ostickets-prereqs/assets/135868956/4cbbfc1c-4918-4c05-90fa-95c16e3395b2">
9. **Install osTicket:**
   - Download osTicket from the Installation Files Folder.
   - Extract and copy the "upload" folder to `C:\inetpub\wwwroot`.
   - Rename the "upload" folder to "osTicket".
   - Reload IIS.
<img width="428" alt="" src="">
<img width="428" alt="" src="">
<img width="428" alt="" src="">
<img width="428" alt="" src="">

10. **Enable PHP Extensions:**
    - Go to sites -> Default -> osTicket in IIS.
    - Enable the following PHP extensions in PHP Manager: 
      - php_imap.dll
      - php_intl.dll
      - php_opcache.dll
<img width="428" alt="" src="">
<img width="428" alt="" src="">

11. **Configure osTicket:**
    - Rename `ost-sampleconfig.php` to `ost-config.php`.
    - Set appropriate permissions for `ost-config.php`.
    - Continue the setup in the browser, providing necessary information except for the Database Settings.
<img width="428" alt="" src="">
<img width="428" alt="" src="">
<img width="428" alt="" src="">
   
12. **Install HeidiSQL:**
    - Download and install HeidiSQL from the Installation Files.
    - Create a new session with root username and Password1.
<img width="428" alt="" src="">
<img width="428" alt="" src="">

13. **Create Database:**
    - Create a new database named `osTicket` in HeidiSQL.
    - Provide the same database name (`osTicket`) in osTicket setup.
<img width="428" alt="" src="">
<img width="428" alt="" src="">

14. **Clean Up:**
    - Delete the `setup` folder from `C:\inetpub\wwwroot\osTicket`.
    - Set permissions of `ost-config.php` to "Read" only.
<img width="428" alt="" src="">
<img width="428" alt="" src="">

15. **Finish Setup:**
    - Login to osTicket in the browser.
<img width="428" alt="" src="">

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

