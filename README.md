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
  - "MySQL 5.5.62" (For this installation, when asked, do a "Typical Setup". After installing, launch Configuration and opt for a "Standard Configuration". It will then ask you to fill in a root password. After which it will then execute the program.
  
  
</p>
<br />

<p>
<img src="https://i.imgur.com/GN6s1ns.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
