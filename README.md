<p align="center">
<img src="https://www.opensourcecms.com/wp-content/uploads/osTicket-logo.png"/>

<h1>osTicket - Prerequisites and Installation</h1>

This is my demonstration on the prerequisites and installation of the open-source help desk ticketing system, osTicket.

<h2>Operating Systems Used</h2>

- <b>Windows 10 Pro, version 22H2<b>


<h2>Environments and Technologies Used</h2>

- <b>Microsoft Azure (Virtual Machines/Compute)</b> 
- <b>Remote Desktop</b>
- <b>Internet Information Services (IIS)</b>

<h2>List of Prerequisites </h2>

- <b>Azure Virtual Machine</b>
- <b>Internet Information Services (IIS)<b>
- <b>PHP Manager<b>
- <b>Rewrite Module<b>
- <b>VC Redist<b>
- <b>MySQL<b>
- <b>Heidi SQL<b>
- <b>osTicket v1.15.8<b>
- <b>Link to downloads: https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6

<h2>Installation Guide:</h2>

<p align="center">
Create a virtual machine using https://portal.azure.com/: <br/>
<img src="https://i.imgur.com/Cn8jYKM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Set up your virtual machine with Windows 10 Pro, version 22H2. Note, you will want to create a virtual machine with at least 2 vCPUs and 16 GB of memory:  <br/>
<img src="https://i.imgur.com/mimMmLT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Connect to the virtual machine by using the public IP address that the VM is set up with. You will connect using the Remote Desktop Connection app: <br/>
<img src="https://i.imgur.com/AYOtlhj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
  <img src="https://i.imgur.com/Y2Qi7jj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
In the virtual machine, download the osTicket-Installation-Files.zip and unzip it onto your desktop. The folder should be called “osTicket-Installation-Files”
We will use the files in this folder to install osTicket and some of the dependencies:  <br/>
<img src="https://i.imgur.com/4WyTJl6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Go to your control panel. From the control panel, open up Programs. Select Turn Windows features on and off:  <br/>
<img src="https://i.imgur.com/suB07eu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/P8VrExq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Install/enable IIS in Windows with CGI and Common HTTP Features, and make sure all Common HTTP Features are checked.
World Wide Web Services -> Application Development Features -> [X] CGI [X] Common HTTP Features:  <br/>
<img src="https://i.imgur.com/jRFBGhm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/UMKNpAK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
To make sure the IIS is installed/enabled, go to a browser of your choice and search for 127.0.0.1. It should look like this:  <br/>
<img src="https://i.imgur.com/m4RzlTH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
1. From the Installation Files, download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0). Go through the install wizard and complete the install. <br />
<br />
2. From the Installation Files, download and install the Rewrite Module (rewrite_amd64_en-US). <br />
<br />
3. Create a folder in the C drive called PHP <br />
<br />
4. From the Installation Files, download PHP 7.3.8 (php-7.3.88-nts-Win32-VC15-x866.zip) and unzip the contents into C:\PHP: <br />
<img src="https://i.imgur.com/1c1MLAb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/7xRJ67X.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Download and install the VC_redist.x86.exe from the installation files. Go through the setup wizard to finish setting up and installing the VC_redist.x86.exe. <br />
<br />
Download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi) Run the setup wizard: Typical Setup -> Launch Configuration Wizard (after install) -> Standard Configuration -> <br />
<br />
Create a password: <br />
<img src="https://i.imgur.com/O3ScTzo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Execute the process on the next page:
<img src="https://i.imgur.com/6omFGyv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Search for IIS in the Windows search bar. Open IIS as an administrator. The program should look like this:
<img src="https://i.imgur.com/FfFLWNi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Register PHP from within IIS. Click on PHP Manager:
<img src="https://i.imgur.com/jrpwfPY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Register a new PHP version:
<img src="https://i.imgur.com/HErPI3l.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Provide a path to the PHP executable file (php-cgi.exe). Go to C Drive -> PHP -> click on php-cgi file:
<img src="https://i.imgur.com/nFQfCiO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Restart the IIS server: <br />
<img src="https://i.imgur.com/tUsuef2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 Install osTicket v1.15.8 -Download osTicket from the Installation Files Folder -Extract and copy the "upload" folder to c:\inetpub\wwwroot -Within c:\inetpub\root, rename "upload" to "osTicket"
<br />
Reload IIS again.
<br />
On IIS go to sites -> Default -> osTicket -On the right, click “Browse *:80”: <br />
<img src="https://i.imgur.com/FhQxTa4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Some extensions are not enabled on the osTicket browser:
<img src="https://i.imgur.com/eFADQWT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Enable the extensions: -Go back to IIS, sites -> Default -> osTicket -Double click PHP manager -Click "Enable or disable an extension": <br />
<img src="https://i.imgur.com/uzEW1PA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/eTHWSdM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Enable three extensions.
<br />
<br />
1.) php_imap.dll
<br />
<br />
2.) php_intl.dll
<br />
<br />
3.) php_opcache.dll:
<br />
<img src="https://i.imgur.com/oEIyqQd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Rename one of the files in our osTicket folder. Go into the file explorer and search for C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
<br />
<br />
Rename the ost-sampleconfig.php to ost-config.php
<br />
<br />
Right-click on the file and go to properties. Click Security, click on Advanced, and disable the inheritance. Select Remove all inherited permissions from this object.
<br />
<br />
Add new permissions.
<br />
<br />
Click Add:
<br />
<img src="https://i.imgur.com/9qTQvYu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Select a principal: <br />
<img src="https://i.imgur.com/YwspbyD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Type "Everyone" in the box (Only type Everyone for this Example):
<img src="https://i.imgur.com/0Rbw93k.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Make sure Full Control and all the other boxes are checked:
<img src="https://i.imgur.com/b12W29J.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Click Apply and Ok: <br />
<img src="https://i.imgur.com/gnvcl4M.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Set up osTicket in the browser. Click Continue on the osTicket browser page. Fill out the page as required, except the Database Settings at the bottom of the page. We will get to that.
<br />
<br />
Download and install HeidiSQL from the Installation Files:
<img src="https://i.imgur.com/2zYUWnk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create a new session in it:
<img src="https://i.imgur.com/IgOXxu8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Make sure the username is root and the password is ROOT:
<img src="https://i.imgur.com/2YRxrOa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Go back to the browser to finish setting everything up. Under the Database Settings in the browser the username will be root and the password will be ROOT.
<br />
<br />
Create a new database within HeidiSQL. In Heidi, right click on the left side where it says "Unnamed", select "create new", and then select "database". Name the new database osTicket. Once we have the new database set up, go back to the osTicket browser and under MySQL Database type in osTicket:
<img src="https://i.imgur.com/zXFKxa2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Log in to osTicket on the browser:
<img src="https://i.imgur.com/MIUPGx6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/TQbjuWv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
End user view: <br />
<img src="https://i.imgur.com/OC85eok.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
osTicket has now been successfully installed!
</p>

<h2>Cleanup:</h2>

<p align="center">
Delete the setup folder in our system. -Delete: C:\inetpub\wwwroot\osTicket\setup. Only delete the setup folder and nothing else.
<br />
<br />
Set the permissions back to "Read" only in the ost-config.php file:
<br />
<img src="https://i.imgur.com/yEeLiva.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<img src="https://i.imgur.com/E5JehE5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
</p>
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
