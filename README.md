<h1>How to Setup a Basic Home Lab Running Active Directory </h1>



<h2>Description</h2>
Project consists of creating a basic homalab Active Directory by creating a Domain, RAS/NAT, and  DCHP Controller
<br />


<h2>Languages and Utilities Used</h2>

- <b>Active Directory</b> 
- <b>Powershell</b>

<h2>Environments Used </h2>
- <b>VirtualBox</b> 
- <b>Windows 10</b> (21H2)
- <b>Windows Server 2022</b>

<h2>Program walk-through:</h2>

<p align="center">
Go to Settings in VirtualBox, found on the top menu as the picture with the gear : <br/>
<br />
<br />
Go  to the Network Option in the side menu
<br />
<br />
For the frist network apadtor select NAT, which will connect the server to the internet:  <br/>
<br />
<br />
For the second network adaptor select select Enable adaptor, in the attached to select Internal Network, and the name intnet. This will connect the server to a internal network in virtualbox <br/>
<br />
<br />
Click the network icon in the far right of the toolbar, the sybmbol a computer monitor with a network jack on the side, click on network, go to change apadtor options. To figure which is which is which <br/>
<br/>
<br/>  
Left click and slect status and then select details, look at the IPv4 address is display, as the internal rounting has not been set up yet <br/>
<br/>
<br/>  
Rename the the first connection to "Internet" , and rename the second connection to internal <br/>
 For the internal connection assign the IP address, by right clicking and go to properties in the drop down menu, double click on Internet Protocol Version 4 (TCP/IPv4) <br/>
Enter the following information <br/> 
  IP Address: 172.16.0.1 <br/>
  Mask: 255.255.255.0 <br/>
  Gateway <blank> <br/>
  DNS: 127.0.0.1 <br/>
<br/>
<br/>  
 Rename the PC, by going to the start menu, go to system, and click on rename this PC, called the Server DC, then click next, and then click restart now, and then click continue <br/>
 Click on Add Role and Features under the Quick Start under Service Manager <br/>
<br/>
<br/>    
 Click Next until you get to the Select destination Server, select the server that you want add the domain controller <br/>
<br/>
<br/>    
 Chose the Active Directory Domain Services, Click next on the next windowe, and then click install after installing click close <br/>
<br/>
<br/>    
 There will a notfication shown a a eclimation mark next to notification flag found on top of Service Manager for post-deployment configuration <br/>
<br/> 
<br/>    
 Choose Adda a new forest under the select deployment operation, and type in the rood domain mame you choose for this project it would be "mydomain.com", click next <br/>
<br/>
<br/>    
 Enter a password it will need to contain a lowercase, upercase, number and special symbol - for strong security, then click next for the next window, and next again,  next again, then click install, After installing the computer will restart <br/>
<br/> 
<br/>    
Create a Administrator instead of using the bulit-in administrator account <br/>
<br/> 
<br/>    
 By Going to the start menu administator tools. and select Active Users and Computer Groups, create a orgination group, and then create new users   Rightclick the new user, and select properties, in the tabs go to member of, click add , type in Member of domain admin and then click okay <br/>
 
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
