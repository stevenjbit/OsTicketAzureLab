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

1. 

<details>

<summary>Expand images</summary>

<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />


</details>


<details>

<summary>Expand images</summary>

<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />

</details>

3. 

<details>

<summary>Expand images</summary>

<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />

</details>

4. 

<details>
<summary>Expand images</summary>

<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />

</details>

5. 

<details>

<summary>Expand images</summary>

<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />

</details>


6. 

<details>
 
 <summary>Expand images</summary>
 
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
 
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
