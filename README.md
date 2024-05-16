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
https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6
</p>-  PHP Manager for IIS 
</p>-  Rewrite Module 
</p>-  PHP 7.3.8
</p>-  VC_redist.x86.exe.
</p>-  MySQL 5.5.62
</p>-  HeidiSQL.
<h2>Installation Steps</h2>

<p>
<p><img width="905" alt="azure" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/1790823e-ec0f-475a-b159-95872c3a6a3b">
</p>
<p>
You will log onto Microsoft Azure and create a resource group after you create a resource group you will create a virtual machine. During the setup phase on Azure please make your virtual machine inside of the resource group you created. Name the virtual machine that you prefer and put the region in the area where you reside. you will be using Windows 10 for this example. When creating a virtual machine I choose a VM with 4 virtual CPUs. you will be prompted to create credentials please write them down so you remember them. In this case, Azure will create the virtual network for us. To finalize everything you will click review and create and your virtual machine will commence being set up on Azure.
  
 <p><img width="692" alt="osticket vm" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/34d97a61-512f-45de-bf6b-2545731ced07">

<p>
<p><img width="1670" alt="Screenshot 2024-05-13 110946" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/4fdc10a4-d554-4a59-979e-863ac450f40a">

</p>
<p>
For this next step, you will use the remote desktop connection protocol to connect to our virtual machine and begin to install our files on the virtual machine. You will go on Azure and get your VMS public IP address. You will copy and paste it on the rdp and log in with the username and password you created when you made the VM on Azure. Once your logged in you will open Microsoft Edge and open the files list that is in the page here. first, you will Install / Enable IIS in Windows WITH CGI and Common HTTP Features. 
You will go to the control panel and find programs and features once you find them you will go to turn the Windows feature on or off. you will look for internet information services and enable it then you will click the collapsible and expand it and go to world wide web services and expand and check cgi. Then go to common http features and check them all on. after this, it will install a web server for the ticket system. To test this type in 127.0.0.1 in Edge it will populate a Windows page that says Internet information services.
</p>
<p><img width="841" alt="progams and features" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/1cff76c4-1b94-4a22-96ef-8ea8b8154e3e">
<p><img width="342" alt="windows iss" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/39e398f0-75ee-40d9-8522-a96d79811079">

<br />

<p>From the Installation Files, download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) after you're done downloading that From the Installation Files, download and install the Rewrite Module (rewrite_amd64_en-US.msi) this is a requirement for OSticket to work.

<p><img width="158" alt="install of rewrite" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/20998d82-26c7-4f7f-a845-171169d1ee2b">

</p>After those files are downloaded you will Create the directory C:\PHP. Go to files and find C drive, create a new folder, and name it php. From the Installation Files, download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP. 
<p><img width="361" alt="extract of php" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/9ac767c6-bf53-46e5-b049-23ccd8186951">

<p>Next steps are From the Installation Files, download and install VC_redist.x86.exe and From the Installation Files, download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi).
</p>
<p><img width="152" alt="c+++" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/e5b28650-9877-4107-9798-77bd5c16c1a4">
<p><img width="160" alt="sql install" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/c371e30d-5d09-416a-8123-7cb9ca98ed72">

</p>Once SQL is done installing you will begin the setup process you will use standard configuration, Create a root password, and remember it. Click Execute and allow the program to deploy the database for the ticket system.
<br />

<p>After the setup is complete Open IIS as an Admin, Register PHP from within IIS, and then reload IIS (Open IIS, Stop and Start the server)
<p><img width="431" alt="iis admin" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/e198eca4-288b-43d5-96a6-d331de4efaa7">
<p><img width="431" alt="php manager" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/e4822e3a-023f-4cc0-9ae7-77b6bfb196d7">
<p><img width="431" alt="php manger 2" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/12946352-88dd-4fe3-80bc-22869fe05121">
<p><img width="431" alt="php3" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/d0da2bdc-72b5-4316-9aae-7cae6a753181">

</p> After you restart the IIS you will Install osTicket v1.15.8, Download osTicket from the Installation Files Folder, Extract and copy the “upload” folder to c:\inetpub\wwwroot, and Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”
<p><img width="538" alt="drag and drop rename" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/64e73d74-cecd-4755-bf95-2923dbc589d8">
<p><img width="359" alt="osticket rename" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/806a9c38-7e8a-409e-adbe-12ebc8471e4b">

<p>
The next step is to Reload IIS (Open IIS, Stop and Start the server). 
</p>
<p><img width="428" alt="server restart" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/14e0773a-db78-44fe-91c8-9a98214bf6c5">
</p> after the restart Go to sites -> Default -> osTicket
On the right, click “Browse *:80” You should get routed to osticket installer webpage 
<p><img width="263" alt="osticket" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/7ee3ff18-ad1d-42ff-8b29-cacbfdc8cc3b">

Note that some extensions are not enabled to enable you: 
<p>
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager


<br />

<p>
<p><img width="320" alt="php enable" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/29c10a03-ae83-4fa4-a597-7812d02da30d">

</p>Click “Enable or disable an extension”
<p>Enable: php_imap.dll
<p>Enable: php_intl.dll
<p>Enable: php_opcache.dll
<p>Refresh the osTicket site in your browse, observe the changes

</p>
<p><img width="322" alt="php enable setting" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/9a208cb2-0cfa-4767-be0e-59b052064abf">

Next, go to files and browse to wwwroot and find Osticker and find ostsampleconfig and Rename: ost-config.php
</p>From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
</p>To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
</p> Next Assign Permissions: ost-config.php
Disable inheritance -> Remove All
New Permissions -> Everyone -> All

<p><img width="247" alt="permisoons" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/bb398aa8-d5ec-44f1-bb27-80cea2624dd7">
<p><img width="294" alt="Screenshot 2024-05-13 122650" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/7f849f0e-1da0-4923-a195-7089ae0041f7">

<br />

<p>After permissions are given you will Continue Setting up osTicket in the browser (click Continue)
</p>Name Helpdesk
</p>Default email (receives email from customers)
</p><img width="263" alt="osticket user" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/9b6e8d2c-1e6c-4389-8eac-81581eebd626">
</p> But before you can finish that set you must set up the database for the SQL so follow these steps. 
</p>From the Installation Files, download and install HeidiSQL.
</p><img width="192" alt="hedisql" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/d447206d-a557-477f-b4aa-cbf6766d4b25">

</p>Open Heidi SQL
</p>Create a new session, root/Password
</p><img width="220" alt="hedisql main setup" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/a1c2fa0f-4d33-4d26-83f6-2bd71ff66652">
</p>Connect to the session
</p>Create a database called “osTicket”
</p><img width="302" alt="osticket creation" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/170a56ff-2f68-4e91-8b35-51a85473415c">

</p> The next steps are to Continue Setting up osticket in the browser
</p>MySQL Database: osTicket
</p>MySQL Username: root
</p>MySQL Password: Password
</p>Click “Install Now!” and you should see this pop-up.
</p><img width="149" alt="install of os" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/d6fe9df4-0b3d-4b68-87e2-2dc5e73d7405">
<p><img width="263" alt="congrats install" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/108373d0-7a0b-44c2-bad4-dc956b54300b">


</p> The next step is to Clean up
<p>Delete: C:\inetpub\wwwroot\osTicket\setup
<p><img width="360" alt="delte setup" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/8e69ae60-4d4b-4dde-8d6c-c4243984c46f">

<p>Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php
<p><img width="295" alt="new permissons" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/a4917cb5-b937-4830-8371-dd764cab4e43">

<p> Use these two URLs to confirm that all went well 
<p>Browse to your help desk login page: http://localhost/osTicket/scp/login.php  
<p>End Users osTicket URL: http://localhost/osTicket/ 
</p>End Users osTicket URL:
</p>http://localhost/osTicket/ 
</p> This is how it will look once you log in: 
</p><img width="272" alt="helpdesk view" src="https://github.com/Angelplascencia007/osticket-prereqs/assets/168943120/0f13ded5-1735-46f1-9136-410c1e30fc76">
</p>That should be all for the ticket install process.
