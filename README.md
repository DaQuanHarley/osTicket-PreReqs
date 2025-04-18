<h1>osTicket - Prerequisites and Installation</h1>

This is my demonstraction on the prerequisites and installation of the open-source help desk ticketing system osTicket.

<h2>Operating Systems Used</h2>

- <b>MacOS (Sequoia 15.4)<b>


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
Setup your virtual machine with Windows 10 Pro, version 22H2. Note, you will want to create a virtual machine with atleast 2 vcpus and 16 gbs of memory:  <br/>
<img src="https://i.imgur.com/mimMmLT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
connect to the virtual machine by using the public ip address the vm is setup with. You will connect using the remote desktop connection app: <br/>
<img src="https://i.imgur.com/AYOtlhj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
  <img src="https://i.imgur.com/Y2Qi7jj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
In the virtual machine download the osTicket-Installation-Files.zip and unzip it onto your desktop. The folder should be called “osTicket-Installation-Files”
We will use the files in this folder to install osTicket and some of the dependencies:  <br/>
<img src="https://i.imgur.com/4WyTJl6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Go to your control panel. From the control panel open up programs. Select, Turn Windows features on and off:  <br/>
<img src="https://i.imgur.com/suB07eu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/P8VrExq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Install / enable IIS in Windows with CGI and Common HTTP Features, make sure all Common HTTP Features are checked.
World Wide Web Services -> Application Development Features -> [X] CGI [X] Common HTTP Features:  <br/>
<img src="https://i.imgur.com/jRFBGhm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/UMKNpAK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
To make sure the IIS is installed / enabled go to a browser of your choice and search for 127.0.0.1 It should look like this:  <br/>
<img src="https://i.imgur.com/m4RzlTH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
1. From the Installation Files, download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0) Go through the install wizard and complete the install. <br />
<br />
2. From the Installation Files, download and install the Rewrite Module (rewrite_amd64_en-US). <br />
<br />
3. Create a folder in the C drive called PHP. <br />
<br />
4. From the Installation Files, download PHP 7.3.8 (php-7.3.88-nts-Win32-VC15-x866.zip) and unzip the contents into C:\PHP <br />
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
Ececute the process on the next page:
<img src="https://i.imgur.com/6omFGyv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/1c1MLAb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


<img src="https://i.imgur.com/1c1MLAb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


<img src="https://i.imgur.com/1c1MLAb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>





  
  
  Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
