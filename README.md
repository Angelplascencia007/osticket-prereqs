<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>
aa
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
https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6
-  PHP Manager for IIS 
-  Rewrite Module 
-  PHP 7.3.8
-  VC_redist.x86.exe.
-  MySQL 5.5.62
-  HeidiSQL.
<h2>Installation Steps</h2>

<p>
<img width="905" alt="azure" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/1790823e-ec0f-475a-b159-95872c3a6a3b">
</p>
<p>
You will log onto Microsoft Azure and create a resource group after you create a resource group you will create a virtual machine. During the setup phase on Azure please make your virtual machine inside of the resource group you created. Name the virtual machine that you prefer and put the region in the area where you reside. We will be using Windows 10 for this example. When creating a virtual machine I choose a VM with 4 virtual CPUs. you will be prompted to create credentials please write them down so you remember them. In this case, Azure will create the virtual network for us. To finalize everything you will click review and create and your virtual machine will commence being set up on Azure.
  
 <img width="692" alt="osticket vm" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/34d97a61-512f-45de-bf6b-2545731ced07">

<p>
<img width="1670" alt="Screenshot 2024-05-13 110946" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/4fdc10a4-d554-4a59-979e-863ac450f40a">

</p>
<p>
For this next step, we will use the remote desktop connection protocol to connect to our virtual machine and begin to install our files on the virtual machine. You will go on Azure and get your VMS public IP address. You will copy and paste it on the rdp and log in with the username and password you created when you made the VM on Azure. Once your logged in you will open Microsoft Edge and open the files list that is in the page here. first, we will Install / Enable IIS in Windows WITH CGI and Common HTTP Features. 
You will go to the control panel and find programs and features once you find them you will go to turn the Windows feature on or off. you will look for internet information services and enable it then you will click the collapsible and expand it and go to world wide web services and expand and check cgi. Then go to common http features and check them all on. after this, it will install a web server for the ticket system. To test this type in 127.0.0.1 in Edge it will populate a Windows page that says Internet information services.
</p>
<img width="841" alt="progams and features" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/1cff76c4-1b94-4a22-96ef-8ea8b8154e3e">
<img width="342" alt="windows iss" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/39e398f0-75ee-40d9-8522-a96d79811079">

<br />

<p>From the Installation Files, download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) after you're done downloading that From the Installation Files, download and install the Rewrite Module (rewrite_amd64_en-US.msi) this is a requirement for OSticket to work.

<img width="158" alt="install of rewrite" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/20998d82-26c7-4f7f-a845-171169d1ee2b">

</p>After those files are downloaded we will Create the directory C:\PHP. Go to files and find C drive, create a new folder, and name it php. From the Installation Files, download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP. 
<img width="361" alt="extract of php" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/9ac767c6-bf53-46e5-b049-23ccd8186951">

<p>Next steps are From the Installation Files, download and install VC_redist.x86.exe and From the Installation Files, download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi).
<img width="152" alt="c+++" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/bf52cd50-ec04-4298-9dc7-a0b76c4a85a9">

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

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
