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
