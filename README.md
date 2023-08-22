# osTicket-Prereqs
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
- Download Required Installation files for osTicket

<h2>Installation Steps</h2>

<p>
<h3>Install the required programs</h3>
<img src="https://i.imgur.com/9KRqPJD.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Make sure you have the following installation files downloaded on the right window.

From the Start Menu, go to "Control Panel" -> "Programs" -> "Turn Windows Features On or Off". Then check the box for "Internet Information Services". Collapse the folder and go to "World Wide Web Services" > Application Development Features" > check the box for "CGI". After checking the box and confirming, collapse the "Common HTTP Features" folder below "Application Development Features", and check to see that every folder is checked. After checking both folders go ahead and input the IP Address, 127.0.0.1, into your internet search browser to confirm that your localhost is working and the Internet Information Services webpage should load.

From there, go ahead and start installing the files on the right folder of the image above in this order:

- "PHPManagerforIIS"
- "Rewrite_amd64"
- "PHP 7.3.8" (For this one you want to create a new folder in your local disk (C:) titled "PHP", and then unzip the contents into the newly-created PHP Folder)
- "VC_redist.x86"
- "MySQL 5.5.62" (For this installation, when asked, do a "Typical Setup". After installing, launch Configuration and opt for a "Standard Configuration". It will then ask you to fill in a root password. After filling out a password, it will then execute the program.
  
  
</p>
<br />

<p>
<h3>IIS Managaer Home</h3>
<img src="https://i.imgur.com/GN6s1ns.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<h3>Register PHP Setup</h3>
<img src="https://i.imgur.com/W7AS6PD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After installing and configuring MySQL, click on the Start Menu and open IIS as an Administrator. The program will look like the first image above. Afterwards, access the PHP Manager button and the 2nd image shown will appear. Click on "Register PHP from Within IIS". To find the PHP, return to the PHP Folder that was created in (C:) and you'll find the PHP-cgi there. Next, under the PHP Extensions section, enable the following extensions
  
  - "php_imap.dll"
  - "php_intl.dll"
  - "php_opcache.dll"
  
  Once that's completed, go back to home on the IIS, look to the right of the IIS program and click on "Restart".
</p>
<br />

<p>
<h3>Transfer 'Upload' Folder to wwwroot</h3>
<img src="https://i.imgur.com/QuqJ5U3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<h3>osTicket on LocalHost</h3>
<img src="https://i.imgur.com/fHvVADz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once the IIS is restarted, go to the osTicket.zip folder that was downloaded earlier and extract the "upload" folder to c:inetpub\wwwroot, as shown in the image above. Once the "upload" folder is copied/moved into the wwwroot folder, change the name of the "upload" folder to "osTicket". Return to the IIS program and from the left side, click on Sites -> Default -> osTicket, and to the right of the IIS program from there, click on "Browse *.80". If all goes well, the osTicket page will load up on your browser.
</p>
<br />

<p>
<h3>ost-sampleconfig.php -> ost-config.php</h3>
<img src="https://i.imgur.com/56sNP4D.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After confirming that the localhost works and osTicket is able to load, go into the osTicket folder placed in wwwroot and look for the following file: "C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php" Once found, first change the file name to "ost-config.php", then open "properties" on the file, go to the "security" tab and click on "Advanced". Disabled the inheritance and after that, add a new principal labeled "everyone". Allow full control access over this file for everyone, and apply.
</p>
<br />

<p>
<h3>osTicket Basic Setup</h3>
<img src="https://i.imgur.com/MgRXcYt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Back to the osTicket browser page, click on "continue" and begin setting up the osTicket system. Make sure the email address for the system settings and the Admin user are NOT the same. Before filling out the Database Settings, install the HeidiSQL file back in the download folder where the rest of the installers are located.
</p>
<br />

<p>
<h3>Creating new Database with  HeidiSQL</h3>
<img src="https://i.imgur.com/BKn5Q13.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
One HeidiSQL is installed and launched, at the bottom left of the program, open a new database. The user is the same as the one in MySQL, "root", and the password will also be the same. This is what the osTicket on the localhost will use as a database. Name the database "osTicket", and click "Open". Once that is completed, return to the osTicket Basic Installation two images above and fill out the remaining MySQL boxes with the same information used when filling out HeidiSQL:
  
  - "MySQL Database: osTicket"
  - "MySQL Username: root"
  - "MySQL Password: ******"
  
Check if everything looks good and click "Install!"
  
<p>
<h3>Completed osTicket System on LocalHost</h3>
<img src="https://i.imgur.com/pf8EZ0W.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<h3>osTicket Login Page</h3>
<img src="https://i.imgur.com/n9vcsiT.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<h3>osTicket Support Page</h3>
<img src="https://i.imgur.com/Klwu0Tl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
If all the steps are done accordingly, the congratuations page will show up. The localhost's login page and support center page will also be working. All that's left to do is to change the permissions on the ost-config file to "read only". Before finishing up, return back to the ost-config.php file (C:\inetpub\wwwroot\osTicket\include\ost-config.php), open up properties -> security -> Advanced, and change the permissions to "read only".
</p>
<br />  
<p>
<h3>Remove osTicket Setup Folder</h3>
<img src="https://i.imgur.com/JwshAcD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The final step before finishing up is to go into the osTicket Folder and delete the "setup" folder, now that the setup for the localhost Ticketing system is complete.
</p>
<br />

<h2>osTicket Part 2</h2>

  - ### [Post-Install Configuration](https://github.com/JCBadion/post-install-config)
