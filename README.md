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

- Windows 10</b> (21H2)

<h2>List of Prerequisites </h2>

- Azure Virtual Machine
- Internet Information Services
- PHP Manager 
- Rewrite Module
- PHP 7.3.8
- VC Redist
- MySQL
- Heidi SQL
- osTicket
- Link to downloads https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6

<h2>Installation Steps</h2>
First of all, Microsoft Azure is used to create a Virtual Machine that uses Windows 10 version 22H2. Your virtual machine should have at least 2 vcpu's and 16gb of memory. Create a username and password that will then be used to log into your virtual machine. (ex: Username: labuser   Password: Labpassword1 )

<p>
<img src="https://i.imgur.com/wu1BW3H.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>


Next, log in to the newly created virtual machine using the Remote Desktop connection in Windows and insert the public IP address of the virtual machine found in the virtual machine details. Press "Use a different account" and input your credentials that you created while making the virtual machine. 
</p>
<img src="https://i.imgur.com/tz6V1UX.png" height="90%" width="90%" alt="Disk Sanitization Steps"/>
</p>

</p>
<br />

<p>
<img src="https://i.imgur.com/czUVgt1.png" height="90%" width="90%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once logged into your virtual machine, you will start to enable Internet Information Services (IIS) by first clicking the windows button on the bottom right and press "Run" or press Ctrl + r. Type in "control" and the control panel menu will pop up.
<p>
<img src="https://i.imgur.com/Lru4kiZ.png" height="65%" width="65%" alt="Disk Sanitization Steps"/>
</p>
<img src="https://i.imgur.com/edcZGE2.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/Q5LSEtf.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<p>
Select "Programs" then under "Programs and Features" press "Turn Windows features on or off". Go down and Enable "Internet Information Services" and click the plus (+) next to Internet Information Services. In the drop-down menu, click the plus (+) next to "World Wide Web Services" and make sure all of the boxes are checked, if not then check all of the boxes. Then click the plus (+) next to "Application Development Features" and check the box next to "CGI" and press Ok. Windows will then apply the changes.
</p>
<img src="https://i.imgur.com/75AFN4O.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/vt5HSCj.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/v9FMisF.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/v81vNpA.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

<br />
To check if you have enabled Internet Information Services (IIS), open the Microsoft Edge browser and in the search bar, type in the IP address 127.0.0.1 . If the following screen shows up, then we can get started on downloading all the prerequisite software.
<p>
<img src="https://i.imgur.com/ygx2wJP.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the installation files provided, first download PHP Manager and open the program from the Downloads in File Explorer. Click next then select "I agree" and let the download finish, you may close the window once it has finished.
</p>
<img src="https://i.imgur.com/bsVwCvM.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<br />
</p>
<p>
Next, download Rewrite Module. Accept the terms and continue to install the program. Press finish to exit the Window.
</p>
<img src="https://i.imgur.com/uOucq60.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create the directory "C:\PHP" in File Explorer by going to "This PC" click into the C:\ drive then right click and make a new folder and rename it "PHP"
</p>
<img src="https://i.imgur.com/4DJGnVR.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/A1RaOlo.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/vCYe2Y2.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now from the installation files, download PHP 7.3.8 and unzip the contents into C:\PHP. To do this, right click on the PHP zip file and press "Extract All" and select the C:\PHP folder that was just created and press Extract.
</p>
<img src="https://i.imgur.com/CTutpgo.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/TqD0hfh.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
*If this appears, choose to "Keep" the file:
</p>
<img src="https://i.imgur.com/JoRcaIi.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/whZTaT7.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, download VC Redist from the installation files.
</p>
<img src="https://i.imgur.com/NlszEUb.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the installation files, download and install MySQL. During the installation process, there will be parts where you can choose different setups, so you will choose the following:
  - Typical Setup
  - Launch Configuration Wizard (after installation)
  - Standard Configuration.
Afterward, it will ask you to set up a password for MySQL and you can use, for example, Password1.
Then press "Execute" to finish the installation.
</p>
<img src="https://i.imgur.com/iIrR1DG.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/QrNETVI.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/jSy4RxS.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/TWFuwld.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
You will then register PHP from within IIS by opening IIS as an Administrator, clicking "PHP Manager" and pressing "Register new PHP version". You will then press the three dots beside the search bar and go to the PHP file that you created in the C:\ drive. Double-click the file that says "php-cgi.exe" and press OK.
</p>
<img src="https://i.imgur.com/OM6xSxY.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/xERgfeN.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/Ytsrcde.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/WlknS6x.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/0bRbalQ.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
On the left side of the IIS Manager, click "VM-osTicket" to return to the home page. Then on the right side under "Actions" -> "Manage Server" restart the server or press stop then start.
</p>
<img src="https://i.imgur.com/Slrx9UT.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the installation files, download osTicket. Open up another File Explorer tab and go to the C:\ drive. From the osTicket zip file, select and drag the "upload" file into the folder c:\inetpub\wwwroot . Then rename the upload folder to "osTicket". Once you rename the folder, open IIS and stop and start the server.
</p>
<img src="https://i.imgur.com/karAugv.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/BkeGCod.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/zX4nzNA.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/vnrkmvL.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
In IIS, on the left, click the drop-down arrow next to "VM-osTicket", then the same with "Sites", as well as on "Default Web Site", and click on "osTicket". On the right-hand side, click "Browse *:80"
</p>
<img src="https://i.imgur.com/svxQari.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
  </p>
<p>
The osTicket Installer will pop up, but notice some extensions are disabled. In ISS, go through Sites -> Default -> osTicket and click on PHP Manager. Click "Enable or disable and extension" and enable these three extensions then refresh the osTicket browser.
- php_imap.dll
- php_intl.dll
- php_opcache.dll


</p>
<img src="https://i.imgur.com/WBrVRTx.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/U34uYAX.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/wc3eZDI.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
  </p>
<p>
One of the files, "ost-sampleconfig.php" now has to be renamed from C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to "ost-config.php". Once renamed, right-click that file and press Properties -> Security -> Advanced, and remove all inheritance. We will now add permissions: Add -> Select a principal -> type "everyone" in the box. Make sure in the Basic permissions that "Full control" is selected and all the boxes are checked, and apply the changes.
</p>
<img src="https://i.imgur.com/Z0p2BKd.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/Ag4zbgg.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
  </p>
<p>
Go back to osTicket and press continue then fill out all the required information besides the Database Settings which we will get to after we download and install Heidi SQL from the installation files. 
</p>
<img src="https://i.imgur.com/jl82UHa.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
Create a new session and make sure the username is "root" and the password is "Password1" as created during MySQL.
<p>
<img src="https://i.imgur.com/efY3D9t.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<img src="https://i.imgur.com/UBC34QA.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<p>
Once the session is created, right-click on "Unnamed" -> Create new -> Database, then rename the database to osTicket. You may now go back to the Database Settings in osTicket and input the database name we just created as well as the username and password for MySQL. Press Install Now
</p>
<img src="https://i.imgur.com/qsBNAYw.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<p>
We will clean up our files by first deleting C:\inetpub\wwwroot\osTicket\setup
<p>
Now set the permissions to read-only in C:\inpetpub\wwwroot\osTicket\include\ost-config.php
<img src="https://i.imgur.com/7YhSdJO.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<p>
Finally, open osTicket in a browser.
</p>
<img src="https://i.imgur.com/2uJJEK6.png height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
You have successfully installed osTicket!
