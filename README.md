# ActiveDirectory-AddUser

<h1>Active Directory Home Lab - Add User</h1>

<h2>Description</h2>
In this lab, I am going to demonstrate how to add users in Active Directory. I will also demonstrate how to add users to a particular group.
<br />


<h2>Software Used</h2>

- <b>Virtual VM VirtualBox</b> 

<h2>Operating Systems Used </h2>

- <b>Windows Server 2019</b>

<h2>Program walk-through:</h2>

<p align="center">
First, open Server Manager and click on 'Tools' on the upper right-hand corner. A dropdown will appear, and click on 'Active Directory Users and Computers'. : <br />
<img src="https://i.imgur.com/wJMopVy.png" height="80%" width="80%" alt="Change System Name"/>
<br />
<br />
A window will open, displaying the new domain I created (mydomain.com). Click on mydomain.com and it will open all the folders to the right. Each folder is categorized by type (eg. organizational unit, container). In an organizational unit type, you can apply group policies to that folder. However, with a container type, you cannot apply group policies. : <br />
<img src="https://i.imgur.com/10w2FXo.png" height="80%" width="80%" alt="Change System Name"/>
<br />
<br />
This is where we will create a new user. Right-click on mydomain.com and go to 'New' and to the right, click on 'User'.  :  <br/>
<img src="https://i.imgur.com/ldheoeV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
A new window will open, displaying the full name for that new user. Originally, the textboxes will be blank for you to fill in. Type in your first, middle, and last name separately, and the textbox for Full Name will automatically fill in. In this case, I used my own name. Next, type in a user logon name (I recommend using your first and last name separated by a period). : <br/>
<img src="https://i.imgur.com/iwDzSAq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
This will now take you to 'Features'. You do not need to add any additional features in this section so click on 'Next'. :  <br/>
<img src="https://i.imgur.com/f8C0Xv5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
The next two sections ('AD DS' and 'DNS Server') do not require any action so click on next for both sections. This will then take you to the 'Confirmation' section, which displays the roles you just added and want to install. First, check the checkbox next to 'Restart the destination server automatically if required'. Then, click on 'Install' and wait for the installation process to complete. This will take some time and the system will automatically restart. :  <br/>
<img src="https://i.imgur.com/D80zygd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Once the installation is complete, you will see a notification on the flag icon (located upper-right corner). Click on that icon and a dropdown menu will appear. Select 'Promote this server to a domain controller', which will allow you to configure the server. :  <br/>
<img src="https://i.imgur.com/zkhZGUo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
After clicking on 'Promote this server to a domain controller', a box should open. This will take you to 'Deployment Configuration'. In this section, select 'Add a new forest'. Next, type the root domain name in the textbox for the new forest. In my case, I used 'mydomain.com'. :  <br/>
<img src="https://i.imgur.com/XxnC5g3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <br />
<br />
In the 'Domain Controller Options' section, type in a password for the Directory Services Restore Mode. Use a password that is easy to remember. This is necessary if you want to restore the AD from backup. Click 'Next'. :  <br/>
<img src="https://i.imgur.com/M4OJvvH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <br />
<br />
In 'Additional Options', the NET BIOS name will be verified. Nothing needs to be done, so click on 'Next' to accept the name. :  <br/>
<img src="https://i.imgur.com/IY4AdO9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br />
<br />
In 'Paths', this will display the default database, log files, and SYSVOL folders. Again, othing needs to be done, so click on 'Next'. :  <br/>
<img src="https://i.imgur.com/MkxB76r.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br />
<br />
The wizard will perform some prerequisite checks to ensure AD can be installed on the server. In this case, the server passed all the checks. There were a few warnings, but that is normal and ok as long as the test passed. Click 'Install' to configure AD on the server. The machine will restart automatically. :
<img src="https://i.imgur.com/0cuunFV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <br />
<br />
Once restarted, you will need to log in with the domain administrator account. Notice how the username displays 'MYDOMAIN\Administrator'. You will log in using the password you created while creating a virtual machine. :  <br/>
<img src="https://i.imgur.com/PTf1YhN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
   <br/>
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
