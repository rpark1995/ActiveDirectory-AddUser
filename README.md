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
A new window will open, displaying the full name for that new user. Originally, the textboxes will be blank for you to fill in. Type in your first, middle, and last name separately, and the textbox for Full Name will automatically fill in. In this case, I used my own name. Next, type in a user logon name (I recommend using your first and last name separated by a period). Click 'Next'. : <br/>
<img src="https://i.imgur.com/iwDzSAq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
You will now be prompted to provide a password for the user. Create a password that is easy for you to remember. Below, you will see a list of checkboxes regarding what to do with the password. You will see that the first checkbox, which requires the user to change the password upon next login, is checked by default. You may uncheck this box if you do not want this option. However, for security purposes, it is recommended to require users to change their password upon next login. Click 'Next' and you will see a summary of the new user's information. Click 'Finish'. :  <br/>
<img src="https://i.imgur.com/QZU1K93.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Going back to the 'Active Directory Users and Computers' window, you can confirm that a new user, Ross Park', has been created. Right-click on the new user and click on 'Properties'. You will see all the information (name, address, member of, etc.) of that new user. :  <br/>
<img src="https://i.imgur.com/7fPOUJr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/wxqurzI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Initially, the new user 'Ross Park' is currently a member of the group 'Domain Users'. To add the user to another group, click 'Add...' and a window should open. In this scenario, I want to add that user to the group 'Domain Admins'. I will type in 'Domain Admins' and select 'Check Names'. When the name becomes underlined, that group exists. Click 'OK'. :  <br/>
<img src="https://i.imgur.com/9ufy98H.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <img src="https://i.imgur.com/wZ64SIJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
When you go back to the Porperties window for the new user, you will see that 'Ross Park' now belongs to both groups. :  <br/>
<img src="https://i.imgur.com/5TEL1nM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <br />
<br />
Before siging in as the new user, I will first log out of the Administrator account. This will then take me to the log on screen. On the log on screen, I will first click on 'Other user' because I am signing in as the new user. Next, I will type in my new user name (ross.park) and my password. :  <br/>
<img src="https://i.imgur.com/DyVnjrJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <img src="https://i.imgur.com/ZiseTsY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <br />
<br />
Now, I am logged in as the new user (ross.park). The Server Manager application will automatically open uopn login. :  <br/>
<img src="https://i.imgur.com/PbiiQt9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
