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

<h2>List of Prerequisites</h2>

- Basic Knowledge of Computers
- Basic navigation knowledge of Azure
- Internet Connection
- Patience and Commitment
  
<h2>Installation Steps</h2>

<p>
![image]https://github.com/Nathantopo01/osticket-prereqs/assets/140284822/2ae6efa5-f53a-4e71-9fe9-2bcb8b47d84c
</p>
<p>
Open up Azure and creat a Virtual Machine, this will automatically create the resource group along with it so do not worry about that.
For this tutorial, we will be going with Windows 10, make sure to select that and continue onwards.
</p>
<br />

<p>
![image](https://github.com/Nathantopo01/osticket-prereqs/assets/140284822/aad04f9e-3f43-483f-bfcb-6fda8865b08a)
</p>
<p>
Next, when asked for sizes, aim to get one with 2 vcpu's and atleast 4 GiB of memory, this will make sure that the Virtual machine runs smoothly and efficently.
At the same time, for the Username and Password, you can create some generic ones like "Nathan1" and "Password1234", as long as you remember them, it does not matter.
</p>
<br />

<p>
![image](https://github.com/Nathantopo01/osticket-prereqs/assets/140284822/8d1d0e74-dd97-4189-811c-2d931b75689e)

</p>
<p>
At the bottom at liscensing, simply checkmark the box and than review + create, and than create again. 
This may take a minute or two to finish so just wait a moment.

</p>

<br />
<p>
![image](https://github.com/Nathantopo01/osticket-prereqs/assets/140284822/4f160788-dc5b-4dde-b43b-04615d432bee)

</p>
<p>
Once it is done creating the virtual machine, navigate to it either through the search bar or by clicking the box of "virtual machine" on the home page.
</p>
<br />

<br />
<p>
![image](https://github.com/Nathantopo01/osticket-prereqs/assets/140284822/2b5070f9-d1f0-47d0-badc-5bb51ea71d42)

</p>
<p>
Here, you are going to click on the Virtual machine you just made and than grab the public ip so that we can connect to it with "remote desktop".
(Your IP will most likely not be the same as mine but that is ok, just make sure you grab yours.)
</p>
<br />

<br />
<p>
![image](https://github.com/Nathantopo01/osticket-prereqs/assets/140284822/bde1fa55-0145-4e38-837f-0989e692fd1b)

</p>
<p>
Go to your search bar in the bottom left of Windows and type in "Remote desktop connection" and run the program and insert your IP.
Directly after this it will ask you for credentials, these are the generic credentials we made earlier so just use those to log in.
Press yes on the next pop-up window.
</p>
<br />

<br />

<p>
You can say no to all of the options and than press accept and move onto the next step.
<p>
FOR THIS NEXT PART MAKE SURE YOU ARE IN THE VIRTUAL MACHINE!
</p>

<br />

<br />
<p>
![image](https://github.com/Nathantopo01/osticket-prereqs/assets/140284822/ce3e8d0e-71d9-4b1d-b547-ebfc1fd4b196)

</p>
<p>
Open up this link in the virtual machine, as this will provide us with all of the nesecarry program materials needed to properly set up osticket. (credit to Josh Madakor)
<p>
https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6
</p>
</p>
<br />

<br />
<p>
![image](https://github.com/Nathantopo01/osticket-prereqs/assets/140284822/b8353fe8-538d-47fd-b95d-95a44760a116)

</p>
<p>
First, download and instal IIS (Internet Information Services), in order to do this, go to the Control panel and than to Programs and then to "Turn Windows featers on or off".
</p>
<br />

<br />
<p>
![image](https://github.com/Nathantopo01/osticket-prereqs/assets/140284822/e9133a64-f91f-45a4-bbf8-f8b319033afd)

</p>
<p>
Navigate to Internet Information Services in the pop-up, check the box, expand that and than expand "World Wide Web Services" and then expand "Application Development Features", check CGI and
then collapse "Application Development Features" and then expand "Common HTTP Features" to checkmark all that is in that dropdown. Press OK. Allow it time to then install the IIS features and than you can close the window.
  <p>
To test that it works real fast, go into the browser and type in the IP "127.0.0.1", if a webpage loads, than it worked perfectly.
  </p>
</p>
<br />
![image](https://github.com/Nathantopo01/osticket-prereqs/assets/140284822/071a718f-9608-49c3-8909-b3039bd70e03)

<br />
</p>
<p>
From the google drive link, download and install "php 7.3.8 ZIP FOLDER".
<p>
<p>
When we extract the filed from this folder, we will be making a new folder in the C: drive named "PHP" and we will be extracting it all to there. 
</p>

</p>
</p>
<br />

<p>
![image](https://github.com/Nathantopo01/osticket-prereqs/assets/140284822/d513bf2f-4a9b-4ca0-818a-e48df4712566)

</p>
<p>
Next, download and instal PHP Manager and Rewrite Module.
<p>
Do the same with "VC redist".
</p>
</p>
<br />

<p>
![image](https://github.com/Nathantopo01/osticket-prereqs/assets/140284822/6d1c3151-8e30-47b6-b39e-c76c73f6a33a)

</p>
<p>
Next on the list is the "mysql-5.5.62", while installing it, make sure to do a Typical Setup, after installed, Launch the Configuration Wizard and do a Standard Configuration, when asked for a password
you can use the same generic password you used earlier to keep everything consistent. (Note that you should NEVER do this with any buisness model.) 
</p>
<br />
<br />

<p>
![image](https://github.com/Nathantopo01/osticket-prereqs/assets/140284822/c425f9b2-134e-422f-a653-8ebd46191da7)

</p>
<p>
Once that is installed and good to go, at the bottom left of the desktop, type in IIS, right click the program and "Run as administrator".
</p>
<br />
<br />

<p>
![image](https://github.com/Nathantopo01/osticket-prereqs/assets/140284822/e16f6cbe-569c-4343-9aae-35f0f8b66389)
![image](https://github.com/Nathantopo01/osticket-prereqs/assets/140284822/e0faecf5-4e6b-4158-9e8d-2e8e9cbc1406)

</p>
<p>
Double click PHP Manager and click "Register new PHP version", once you do this, navigate to the previous PHP Folder we extracted that zip folder into and selece the "php-cgi" application.
</p>
<br />
<br />

<p>
![image](https://github.com/Nathantopo01/osticket-prereqs/assets/140284822/c3138526-cd8a-44dc-92a7-d6399e515548)

</p>
<p>
Back to the google drive, download "osTicket". Open up two seperate file explorer windows, with the first one go into the osTicket zip file and keep it open seeing the folders "script" and "upload". On the second file explorer navigate to "C:\inetpub\wwwroot" and drag the upload folder into it. This process will take a moment.
</p>
<br />
<br />

<p>
![image](https://github.com/Nathantopo01/osticket-prereqs/assets/140284822/792c0e84-44b0-450e-829f-d534f5aeed82)

</p>
<p>
VERY IMPORTANT, once the upload folder is done going into the wwwroot, RENAME THE "upload" FOLDER TO "osTicket".
</p>
<p>
![image](https://github.com/Nathantopo01/osticket-prereqs/assets/140284822/a3d8e771-ddf4-40bd-945f-4d43ea951a7e)

Restart IIS.
</p>
<br />
<br />

<p>
![image](https://github.com/Nathantopo01/osticket-prereqs/assets/140284822/f17da7ea-d853-4289-ac46-0f7aee0f813c)

</p>
<p>
Inside of ISS, on the left bar, go to Sites, Default Web Site, osTicket, and than on the right, select Browse .80.
</p>
<br />
<br />

<p>
![image](https://github.com/Nathantopo01/osticket-prereqs/assets/140284822/5ecef1a2-8861-4836-ad55-2967d9a7116b)

</p>
<p>
Some extensions will still have an X on them, to fix them we need to enable them in IIS, go to IIS and under the osTicket folder, go to PHP Manager
</p>
<br />
<br />

<p>
![image](https://github.com/Nathantopo01/osticket-prereqs/assets/140284822/de22c419-cfab-4250-81a9-b197a521e9db)

</p>
<p>
Go to "Enable or Disable extension and enable "php_imap", "php_intl", and "php_opcache".
</p>
<br />
<br />


<p>
Go back to the osTicket in the browser and refresh the page to see that the X are now checkmarks. (We will not be getting rid of all of the X)
</p>
<br />
<br />

<p>
![image](https://github.com/Nathantopo01/osticket-prereqs/assets/140284822/f1f91883-c0b4-4c43-b8ea-d4f48cbd00d3)

</p>
<p>
Navigate through files to get to "C:\inetpub\wwwroot\osTicket\include" and rename "ost-sampleconfig" to "ost-config".
</p>
<br />
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
