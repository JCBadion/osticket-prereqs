# osticket-prereqs
Prerequisites for installing osTicket

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

- Windows 10</b> (22H2)

<h2>List of Prerequisites</h2>

- Setup Virtual Machine (VM)
- Remote Access to VM
- Download Required Installation files
- Item 4
- Item 5

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/9KRqPJD.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Make sure you have the following installation files downloaded on the right window.

From the Start Menu, go to "Control Panel" > "Programs" > "Turn Windows Features On or Off". Then check the box for "Internet Information Services". Open the folder and go to "World Wide Web Services" > Application Development Features" > check the box for "CGI". After checking the box and confirming, go ahead and input your IPv4 Address into your internet search browser to confirm that your localhost is working and the Internet Information Services webpage should load.
  
From there we will go ahead and start installing the files on the right folder of the image above in this order:

  - "PHPManagerforIIS"
  - "Rewrite_amd64"
  - "PHP 7.3.8" (For this one you want to create a new folder in your local disk (C:) titled "PHP", and then unzip the contents into the newly-created PHP Folder)
  - "VC_redist.x86"
  - "MySQL 5.5.62" (For this installation, when asked, do a "Typical Setup". After installing, launch Configuration and opt for a "Standard Configuration". It will then ask you to fill in a root password. After filling out a password, it will then execute the program.
  
  
</p>
<br />

<p>
<img src="https://i.imgur.com/GN6s1ns.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After installing and configuring MySQL, click on the Star Menu and open IIS as an Administrator. The program will look like the image above. Afterwards, access the PHP Manager and click on "Register PHP from Within IIS". To find the PHP, return to the PHP Folder that was created in (C:) and you'll find the PHP.exe there. Once that's completed, look to the right of the IIS and click on "Restart".
</p>
<br />

<p>
<img src="https://i.imgur.com/QuqJ5U3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once the IIS is restarted, go to the osTicket.zip folder that we downloaded earlier and extract the "upload" folder to c:inetpub\wwwroot, as shown in the image above. Once the "upload" folder is copied/moved into the wwwroot folder, change the name of the "upload" folder to "osTicket". Return to the IIS program and from the left side, click on sites -> Default -> osTicket, and to the right of the IIS program from there, click on "Browse *.80". If all goes well, the osTicket page will load up on your browser.
</p>
<br />

<p>
<img src="https://i.imgur.com/fHvVADz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
