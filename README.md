<p align="center">
<img src="https://i.ytimg.com/vi/K7T_JjvEamg/maxresdefault.jpg" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
The developer of osTicket, Enhancesoft, is a software firm that specializes in providing outstanding help desk solutions that enable organizations to concentrate on what matters most. The osTicket open-source help desk ticketing system installation process is described in this tutorial. <br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Microsoft Azure
- Virtual Machine
- osTicket Installation Files [link](https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)


<h2>Installation Steps</h2>


<h3>Step 1: Connect to your Virtual Machine with Remote Desktop</h3>

- Please go to my instruction if you require assistance connecting to your virtual machine. [here](https://github.com/haleypruittcc/ResourcegroupandHelloworld)

<h3>Step 2: Install and activate Windows' IIS (Internet Information Services) </h3>

<p align="center">
<img src="https://i.imgur.com/iEIhTMo.png" height="80%" width="80%" alt="Azure Free Account"/> 
</p>


- First, Go to the bottom of the search bar beside the start and search "Control Panel". 
- Next, click on "Programs" then, select  "Turn Windows features on or off".
- Next, open Internet Information Services > World Wide Web Services > Application Development Features > check the box on "CGI".
- Finally, select "Ok"





<h3>Step 3:  Download and Installtion Files of the Web Platform Installer
</h3>

<p align="center">
<img src="https://i.imgur.com/mdLy4c3.png" height="80%" width="80%" alt="Azure Free Account"/> 
</p>


- Here are the osTicket Installation Files [link](https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)
- First, Download "PHP Manager for IIS " > Select a "Download"  
- You will then follow a prompt to install "PHP Manager for IIS "

<p align="center">
<img src="https://i.imgur.com/oRyUssH.png" height="80%" width="80%" alt="Azure Free Account"/> <img src="https://i.imgur.com/065U0Xv.png" height="80%" width="80%" alt="Azure Free Services"/>
</p>

- Next, Download " Rewrite Module" > Select "Download"
- Create a folder and name ie "PHP" by go to " this PC" > then create the folder in "Window C".


<p align="center">
<img src="https://i.imgur.com/Dl3xNJM.png" height="80%" width="80%" alt="Azure Free Account"/> 
</p>

- Next, Download "PHP 7.3.8"
- Once it done download right the file and select "Extract All" 
- Then, click on "Browse" and extract the file that create in the last step "PHP" file and click "Extract"


<p align="center">
<img src="https://i.imgur.com/DvyiEeW.png" height="80%" width="80%" alt="Azure Free Account"/> 
</p>

- Next, Download "VC_redist.x86.exe" > Select "Download"
- You will then follow a prompt to install "VC_redist.x86.exe"

<p align="center">
<img src="https://i.imgur.com/y5qv9Mn.png" height="80%" width="80%" alt="Azure Free Account"/> 
</p>

<p align="center">
<img src="https://i.imgur.com/BU8JC2I.png" height="80%" width="80%" alt="Azure Free Account"/> 
</p>

<p align="center">
<img src="https://i.imgur.com/d5KeP4Z.png" height="80%" width="80%" alt="Azure Free Account"/> 
</p>

<p align="center">
<img src="https://i.imgur.com/n5QsaKk.png" height="80%" width="80%" alt="Azure Free Account"/> 
</p>



- Next, Download "My SQL 5.5.62" > Select "Typical Setup"
- Then, Select " Standard Configuration" > type any password that you can easily rememeber.
  - Example: "Password1"
- Then you going to contiue follow the prompts to install.

<h3>Step 4:  Reload IIS and Enable  Extensions in IIS
</h3>


<p align="center">
<img src="https://i.imgur.com/JB3Cbrc.png" height="80%" width="80%" alt="Azure Free Account"/> 
</p>

<p align="center">
<img src="https://i.imgur.com/0mY23yA.png" height="80%" width="80%" alt="Azure Free Account"/> 
</p>

<p align="center">
<img src="https://i.imgur.com/Uacc8HW.png" height="80%" width="80%" alt="Azure Free Account"/> 
</p>

<p align="center">
<img src="https://i.imgur.com/MTMZ44V.png" height="80%" width="80%" alt="Azure Free Account"/> 
</p>

<p align="center">
<img src="https://i.imgur.com/4B5mjnt.png" height="80%" width="80%" alt="Azure Free Account"/> 
</p>

<p align="center">
<img src="https://i.imgur.com/NeIlauO.png" height="80%" width="80%" alt="Azure Free Account"/> 
</p>


<p align="center">
<img src="https://i.imgur.com/4v16Ssz.png" height="80%" width="80%" alt="Azure Free Account"/> 
</p>

- Install osTicket v1.15.8
  - Download osTicket from the Installation Files Folder
  - Extract and copy “upload” folder to c:\inetpub\wwwroot
  - Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”
- First, open IIS as Admin and Register PHP from within IIS.
- Next, reload IIS (Open IIS, Stop and Start the server) 
- Reload IIS (Open IIS, Stop and Start the server)
- Go to sites -> Default -> osTicket and on the right, click “Browse *:80”
- Go back to IIS, sites -> Default -> osTicket
- Double-click PHP Manager and Click “Enable or disable an extension”
  - Enable: php_imap.dll
  - Enable: php_intl.dll
  - Enable: php_opcache.dll
- Refresh the osTicket site in your browse, observe the changes
- Rename: ost-config.php by going to This PC -> Windows(:C) -> intepub -> wwwroot -> osTicket -> inclube then scroll down to find "ost-sampleconfig.php"
  - From: ost-sampleconfig.php -> To: ost-config.php.

<p align="center">
<img src="https://i.imgur.com/4Nli569.png" height="80%" width="80%" alt="Azure Free Account"/> 
</p>

- Assign Permissions: ost-config.php by going to 
  - Disable inheritance -> Remove All
  - New Permissions -> Everyone -> All

<h3>Step 5:  
</h3>



