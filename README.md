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
<a href="https://imgur.com/xX5ax4x"><img src="https://i.imgur.com/xX5ax4x.png" title="source: imgur.com" /></a>
</p>
<p>
Open up Azure and creat a Virtual Machine, this will automatically create the resource group along with it so do not worry about that.
For this tutorial, we will be going with Windows 10, make sure to select that and continue onwards.
</p>
<br />

<p>
<a href="https://imgur.com/SWMaJ0I"><img src="https://i.imgur.com/SWMaJ0I.png" title="source: imgur.com" /></a>
</p>
<p>
Next, when asked for sizes, aim to get one with 2 vcpu's and atleast 4 GiB of memory, this will make sure that the Virtual machine runs smoothly and efficently.
At the same time, for the Username and Password, you can create some generic ones like "Nathan1" and "Password1234", as long as you remember them, it does not matter.
</p>
<br />

<p>
<a href="https://imgur.com/6kOjo3R"><img src="https://i.imgur.com/6kOjo3R.png" title="source: imgur.com" /></a>

</p>
<p>
At the bottom at liscensing, simply checkmark the box and than review + create, and than create again. 
This may take a minute or two to finish so just wait a moment.

</p>

<br />
<p>
<a href="https://imgur.com/QYSsNza"><img src="https://i.imgur.com/QYSsNza.png" title="source: imgur.com" /></a>

</p>
<p>
Once it is done creating the virtual machine, navigate to it either through the search bar or by clicking the box of "virtual machine" on the home page.
</p>
<br />

<br />
<p>
<a href="https://imgur.com/C4p9ws4"><img src="https://i.imgur.com/C4p9ws4.png" title="source: imgur.com" /></a>

</p>
<p>
Here, you are going to click on the Virtual machine you just made and than grab the public ip so that we can connect to it with "remote desktop".
(Your IP will most likely not be the same as mine but that is ok, just make sure you grab yours.)
</p>
<br />

<br />
<p>
<a href="https://imgur.com/2cIpbCy"><img src="https://i.imgur.com/2cIpbCy.png" title="source: imgur.com" /></a>

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
<a href="https://imgur.com/NHUCzE8"><img src="https://i.imgur.com/NHUCzE8.png" title="source: imgur.com" /></a>

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
<a href="https://imgur.com/AMUSaAa"><img src="https://i.imgur.com/AMUSaAa.png" title="source: imgur.com" /></a>

</p>
<p>
First, download and instal IIS (Internet Information Services), in order to do this, go to the Control panel and than to Programs and then to "Turn Windows featers on or off".
</p>
<br />

<br />
<p>
<a href="https://imgur.com/oIzfpHy"><img src="https://i.imgur.com/oIzfpHy.png" title="source: imgur.com" /></a>

</p>
<p>
Navigate to Internet Information Services in the pop-up, check the box, expand that and than expand "World Wide Web Services" and then expand "Application Development Features", check CGI and
then collapse "Application Development Features" and then expand "Common HTTP Features" to checkmark all that is in that dropdown. Press OK. Allow it time to then install the IIS features and than you can close the window.
  <p>
To test that it works real fast, go into the browser and type in the IP "127.0.0.1", if a webpage loads, than it worked perfectly.
  </p>
</p>
<br />
<a href="https://imgur.com/yjA1xLM"><img src="https://i.imgur.com/yjA1xLM.png" title="source: imgur.com" /></a>

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
<a href="https://imgur.com/8zEQoH2"><img src="https://i.imgur.com/8zEQoH2.png" title="source: imgur.com" /></a>

</p>
<p>
Next, download and instal PHP Manager and Rewrite Module.
<p>
Do the same with "VC redist".
</p>
</p>
<br />

<p>
<a href="https://imgur.com/9h0HTCg"><img src="https://i.imgur.com/9h0HTCg.png" title="source: imgur.com" /></a>

</p>
<p>
Next on the list is the "mysql-5.5.62", while installing it, make sure to do a Typical Setup, after installed, Launch the Configuration Wizard and do a Standard Configuration, when asked for a password
you can use the same generic password you used earlier to keep everything consistent. (Note that you should NEVER do this with any buisness model.) 
</p>
<br />
<br />

<p>
<a href="https://imgur.com/J5H5uFV"><img src="https://i.imgur.com/J5H5uFV.png" title="source: imgur.com" /></a>

</p>
<p>
Once that is installed and good to go, at the bottom left of the desktop, type in IIS, right click the program and "Run as administrator".
</p>
<br />
<br />

<p>
<a href="https://imgur.com/ZBuBcsV"><img src="https://i.imgur.com/ZBuBcsV.png" title="source: imgur.com" /></a>
<a href="https://imgur.com/VTOCYPb"><img src="https://i.imgur.com/VTOCYPb.png" title="source: imgur.com" /></a>

</p>
<p>
Double click PHP Manager and click "Register new PHP version", once you do this, navigate to the previous PHP Folder we extracted that zip folder into and selece the "php-cgi" application.
</p>
<br />
<br />

<p>
<a href="https://imgur.com/iswD4su"><img src="https://i.imgur.com/iswD4su.png" title="source: imgur.com" /></a>

</p>
<p>
Back to the google drive, download "osTicket". Open up two seperate file explorer windows, with the first one go into the osTicket zip file and keep it open seeing the folders "script" and "upload". On the second file explorer navigate to "C:\inetpub\wwwroot" and drag the upload folder into it. This process will take a moment.
</p>
<br />
<br />

<p>
<a href="https://imgur.com/71Jhytz"><img src="https://i.imgur.com/71Jhytz.png" title="source: imgur.com" /></a>

</p>
<p>
VERY IMPORTANT, once the upload folder is done going into the wwwroot, RENAME THE "upload" FOLDER TO "osTicket".
</p>
<p>
<a href="https://imgur.com/NyA0KdI"><img src="https://i.imgur.com/NyA0KdI.png" title="source: imgur.com" /></a>

Restart IIS.
</p>
<br />
<br />

<p>
<a href="https://imgur.com/Evv04nq"><img src="https://i.imgur.com/Evv04nq.png" title="source: imgur.com" /></a>

</p>
<p>
Inside of ISS, on the left bar, go to Sites, Default Web Site, osTicket, and than on the right, select Browse .80.
</p>
<br />
<br />

<p>
<a href="https://imgur.com/sXg10fx"><img src="https://i.imgur.com/sXg10fx.png" title="source: imgur.com" /></a>

</p>
<p>
Some extensions will still have an X on them, to fix them we need to enable them in IIS, go to IIS and under the osTicket folder, go to PHP Manager
</p>
<br />
<br />

<p>
<a href="https://imgur.com/gY8XxFF"><img src="https://i.imgur.com/gY8XxFF.png" title="source: imgur.com" /></a>

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
<a href="https://imgur.com/RtfAuj1"><img src="https://i.imgur.com/RtfAuj1.png" title="source: imgur.com" /></a>

</p>
<p>
Navigate through files to get to "C:\inetpub\wwwroot\osTicket\include" and rename "ost-sampleconfig" to "ost-config".
</p>
<br />
<br />

<p>
Right click the file, go to properties, security, and than advanced and disable inheritence. Press to remove all inheritence.
</p>
<br />
<br />

<p>
<a href="https://imgur.com/gk75APQ"><img src="https://i.imgur.com/gk75APQ.png" title="source: imgur.com" /></a>

</p>
<p>
Click on Principal, type "everyone" in the box, press ok, and then enable all of the boxes. (You can not enable "special permissions") Press ok ok and go back to the osTicket browser.
</p>
<br />
<br />

<p>
<a href="https://imgur.com/zxuOJN7"><img src="https://i.imgur.com/zxuOJN7.png" title="source: imgur.com" /></a>

</p>
<p>
Helpdesk name does not amtter so ahve fun with it, you can make up an email as well just make sure to write it down like "nathan@helpdesk.com". Fill out and remember the rest of the information.
</p>
<br />
<br />

<p>
Go back to the google drive to download and install "HeidiSQL". You will be installing everything and it does not need to go to a special folder so just click the next button for this one.
</p>
<br />
<br />

<p>
<a href="https://imgur.com/ZH0UX2k"><img src="https://i.imgur.com/ZH0UX2k.png" title="source: imgur.com" /></a>

</p>
<p>
With the new program open, click new and put in the username and password you put in when installing the SQL server.
</p>
<br />
<br />

<p>

</p>
<p>
In the program, right click "Unnamed" and than "create new" "database", and name it "osTicket".
</p>
<br />
<br />

<p>

</p>
<p>
Back in the browser, in the bottom section the SQL username is root (make sure it is not capitalized), and the password is wahtever you set it up to be, and than make the database name "osTicket". You can now finally press that "Install now" Button.
</p>
<br />
<br />

<p>
</p>
<p>
We just need to do some finishing touches, navigate to the folder "C:\inetpub\wwwroot\osTicket" and delete the "setup" folder.
  <p>
<a href="https://imgur.com/5DTGr45"><img src="https://i.imgur.com/5DTGr45.png" title="source: imgur.com" /></a>

Then in "C:\inetpub\wwwroot\osTicket\include", set the permissions in ost-config.php to "read only". Press OK and you are now done with the initial installation!
<p>
To make sure the system works, you can go to "http://localhost/osTicket/" and login with the previously made login info you made to verify it.
  </p>
</p>
<br />
