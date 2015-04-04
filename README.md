# Create-a-Mapped-Drive-on-a-Domain

1.	Open Active Directory Users and Computers and Group Policy Management
2.	In the Group Policy Management right click the OU or Group you wish to edit
3.	Click Create a GPO in this domain, and Link it here..
4.	Assign it a name 
5.	Click Okay
6.	Right click on new policy and click Edit
7.	Click User Configuration follow the path:
a.	User Configuration > Preferences > Windows Settings > Drive Maps
8.	Right Click in the empty space and click New > Mapped Drive
9.	Under the General Tab click Create next to Action: 
10.	For location point it to the shared folder. 
  a.	\\ServerName\Folder
  b.	Example: \\CS-ADSERVER\Software
11.	Select the Drive Letter (choose any letter)
12.	Under Hide/Show this drive click Show this drive
13.	Under Hide/Show all drives click Show all drives
14.	Click Apply
15.	To select users and groups select the Common tab
16.	Click Item-level targeting 
17.	Click Targeting
18.	Select New Item
19.	Select User
20.	Browse for specific user in his/her specific group 
  a.	Example how it should read:
  i.	the user is <username> (SID match)
  AND the user is a member of the security group <group name>
21.	Click OK
22.	Select the General tab and click OK
23.	Log into the specified user account
24.	Once logged in open a command prompt
25.	Type gpupdate /force (this will force a group policy update) 
26.	Done
