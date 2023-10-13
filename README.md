<h1>OsTicket Lab on Azure</h1>

<h2>Description</h2>
In this lab we will install a ticketing system on a local server that is running on a Windows 10 Pro virtual machine. For this project, we will be utilizing OsTicket as our ticketing software and Microsoft's Azure as our cloud platform to spin up our virtual machine. We will also utilize Internet Information Services (IIS), MySQL and Heidi SQL to set up our local server so that we can access our ticketing system from a web browser like a portal. By the end of this lab, our setup will resemble any ticketing system utilized for the technical support operations of an IT department and can serve as an environment to explore and learn the parameters of working a ticket for an IT Help Desk Technician. 
<br><br>
We will first create a virtual machine on Microsoft Azure, choosing Windows 10 Pro as our Operating System which will enable us to set up a local server. Then, we will access this VM from our own personal computer through Microsoft's Remote Desktop Connection. After we are connected, we will set up and configure a local server to act as a host for our ticketing system application, using IIS, MySQL and Heidi SQL. This will allow us to create a webpage to act as our portal. Finally, we will install OsTicket, and configure it to resemble a standard environment for a ticketing system. We will achieve this by creating:
<br><br>
- Users who have issues and access the portal to create tickets
<br>
- Technical support agents who respond to the tickets and close them out
<br>
- A system administrator who manages Service Level Agreements (SLAs), creates teams of Help Desk Agents assigned to different IT areas, and assigns the tickets to agents as they come in. 
<br><br>
Configuring and running this lab will help to develop our comprehension of how to set up, configure and operate a typical ticketing system, along with building our confidence in working tickets to resolve technical support requests, using a Remote Desktop Connection, introducing us to using a server, and finally using a cloud platform for our computing needs.
</br>

<h2>Software and Utilities Used</h2>

- <b>Microsoft Azure</b>
- <b>Remote Desktop Connection</b>
- <b>Windows 10 Pro</b> (22H2)
- <b>Internet Information Services (IIS)</b>
- <b>MySQL</b>
- <b>Heidi SQL</b>
- <b>Visual C++ Redistributible</b>
- <b>OsTicket</b>

<h2>Program walk-through:</h2>

<details>

<summary>Network and VM Diagram</summary>

<img src="" height="80%" width="80%" />


</details>

1. Our first step in the lab will be to create a Resource group on Azure, and then create a Virtual Machine running Windows 10 pro within that resource group. After entering the parameters we want, with an easy to remember user name and password (suitable for our testing environment, not in real usage where passwords should be more complex) and reviewing the set up, press create and allow some time for the machine to spin up. After that is done, on our personal computer, we will open Remote Desktop Connection (whether Windows or Mac) and enter the public IP address we copied from the overview screen of our VM. A screen will pop asking us to connect anyway, where we will hit yes, and then another one will ask us for our credentials. After we adjust the privacy settings on Windows required for the first time use, we will be into a standard Windows desktop environment, ready for our next step. 

<details>

<summary>Expand images</summary>

<img src="https://i.imgur.com/ghVNMmZ.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/HulY6H8.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/9e1n0U6.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/S7YaF1l.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/D7UjWNV.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/8Xis8Eo.jpg" height="80%" width="80%" />


</details>

2. Our next step will be to enable IIS in Windows with CGI, Common HTTP Features and IIS Management Console. To do that, first open the control panel, and go to Programs. There, under programs or features, we will go to "Turn Windows Features on or off" and in the pop-up go down to World Wide Web Services->Application Development Features->Select CGI. Next we will go to another subfolder in World Wide Web Services->Common HTTP Features and select every feature. After those selections, hit "OK" and the Windows Features screen will say these changes have been completed. Then we will enable IIS Management Console by going to Internet Information Services -> Web Management Tools -> IIS Management Console and select IIS Management Console. After that we will select OK, and then we can open up the Edge browser, select the privacy/information settings desired, and enter the Home/Loopback address 127.0.0.1 to see that we have IIS enabled. 

<details>

<summary>Expand images</summary>

<img src="https://i.imgur.com/vfiGyh3.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/Z0kInxM.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/H9c8PJz.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/nSedYuE.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/tJcOfSW.jpg" height="80%" width="80%" />

</details>

3. After setting up IIS, we can download and install PHP Manager for IIS and the Apache rewrite module. Then, after downloading PHP 7.3.8, in the C: drive of our VM, create the directory C:\PHP, and unzip the contents into that folder. Then we will download and install Microsoft Visual C++ redistributable. Next, download MySQL Server 5.5 and launch the intallation wizard, choosing a typical setup and configuration, and choosing an easy-to-remember password. After all that, we can open IIS as an Administrator, register PHP from within IIS, and reload IIS, stopping and restarting the server. Our local server should now be running and we can install OsTicket.

<details>

<summary>Expand images</summary>

<img src="https://i.imgur.com/lfB20ti.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/K2cr2Je.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/8lw6bJE.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/GkM7LaG.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/DuCVa9k.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/2TuVoWD.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/ggXfZfV.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/h5QdzB7.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/C8x4cWs.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/pinOt39.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/kTUYPku.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/4NPrMGG.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/hsXnkA1.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/N4OWFaP.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/nI8LmQb.jpg" height="80%" width="80%" />

</details>

4. To install OsTicket (in this case v1.15.8), download the software, and from the download folder, extract and copy the "upload" folder into C:\inetpub\wwwroot. Within that folder, rename "upload" to "osTicket". Reload IIS after that, by opening it up, stopping then restarting the server. Next, go to sites -> Default -> osTicket, and on the right, click "Browse *:80". This will load the software to run on our server. However, as we can see on our browser, some necessary extensions for OsTicket are not enabled, so we will change that. Back on IIS, click on sites -> Default -> osTicket, double click "PHP Manager", click "Enable or disable an extension" and enable php_impad.dll, php_intl.dll, php_opcache.dll. After refreshing the osTicket site in our browser, we can see some changes. Finally, we will rename ost-config.php by changing in file explorer C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to C:\inetpub\wwwroot\osTicket\include\ost-config.php. Then right clicking on this file, we will change the permissions by disabling inheritance -> Remove All and add New Permissions -> Everyone -> All.  

<details>
<summary>Expand images</summary>

<img src="https://i.imgur.com/Fr1jNi4.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/JfsAgoc.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/rkWUYx8.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/7K5Sr2D.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/MR0qnHg.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/T5uLtco.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/BNxouS0.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/lMZ3vkA.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/aT2rekg.jpg" height="80%" width="80%" />

</details>

5. Now we can finalize the setup of OsTicket on our server. First we will continue with the install of OsTicket on our browser by inputting the Name of "Helpdesk" and a default email. Then we will download and install HeidiSQL (our version was 12.3.0.6589), open it, create a new session with "root/Password12345", connect to the session, and create a database called "osTicket". Then we can go back to the browser and finalize OsTicket. Input "osTicket" in MySQL database, "root" in MySQL Username and "Password12345" (or whatever you like) in MySQL Password, and click "Install Now!". Finally our setup of OsTicket is ready to explore (hopefully with no errors!), so we should just clean it up by deleting C:\inetpub\wwwroot\osTicket\setup and on C:\inetpub\wwwroot\osTicket\include\ost-config.php set permissions to "Read" only. Browse to http://localhost/osTicket/scp/login.php to see if our portal is operating as it should!

<details>

<summary>Expand images</summary>

<img src="https://i.imgur.com/3b5zjf3.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/NPJOrDD.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/2RzdHrk.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/PPt2yhw.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/ErFZ4yM.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/2spSyi9.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/I6rfvyZ.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/qHeYh1O.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/h7MqZkt.jpg" height="80%" width="80%" />

</details>

6. Now that OsTicket is installed, we can login through the portal using our admin credentials we chose earlier. Entering it, we see the first "ticket" is a welcome message. The first step in our administrative tasks is to create roles. Roles are the permissions granted to Agents per Department that they have access to. Let's create a role called "Supreme Admin" with all the permissions available. Then, we can create a new department. Departments are where tickets are routed through. We will create one called "System Administrators", which we can set to receive all tickets. Next we can create Teams. Teams allow you to pull Agents from different Departments and organize them to handle a specific issue, so for example, we could create a team of Tier II agents who are the Subject Matter Experts (SMEs) from different departments. Let's do that, as a Level I Support Team is already created. Now we can create some agents. Agents are given access to the help desk with the intent to respond and resolve the tickets. We'll create Jane and John, and assign them certain permissions. Our next step is to create some users, who will represent customers or perhaps employees from other departments of a company. Users are the ticket owners of the tickets in the help desk. When a ticket is created, their email address will be associated with the ticket for communication purposes. For our second last step we can create a Service Level Agreement (SLA) plan. The purpose of the SLA Plan is to provide a length of time in which the help desk Administrator expects tickets to be closed. We will create SEV-A, SEV-B and SEV-C with typical response periods depending on the severity of the incident: from 24/7 within an hour, to 24/7 within 4 hours to 9-5 business days within 8 hours, respectively. Finally, we will create some "Help Topics", which are intended for users to select the type of issue they are experiencing, helping to streamline the help desk operations. 
<br><br>
We now have a nicely configured help desk to test out. Let's create a few tickets and see how to work a ticket as a help desk technician!

<details>
 
 <summary>Expand images</summary>
 
<img src="https://i.imgur.com/F3wqaB1.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/2QtwUCJ.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/e1myDBV.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/6eac90w.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/Tv5qWdR.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/A8AHYYZ.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/NCpTHsp.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/qYtqiX2.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/SDuf2IX.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/VzwjbPY.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/7u5QPiI.jpg" height="80%" width="80%" />
<img src="https://i.imgur.com/Isazh8C.jpg" height="80%" width="80%" />
 
 </details>
 
7. 
 
 <details>
  
  <summary>Expand images</summary>
  
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />

 </details>
 
 8.  
 
 <details>
 
 <summary>Expand images</summary>
 
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />

</details>

9. 

<details>
 
 <summary>Expand images</summary>
 
 <img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
 
 </details>
 
 <br><br>Our lab is now hopefully functioning just as our initial diagram, and we can explore our set up!

</br>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
