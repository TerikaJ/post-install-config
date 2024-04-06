<p align="center">
<img src="https://i.imgur.com/KzJbWRS.png" height="50%" width="50%" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Installation Configuration</h1>

This demonstration outlines the post-install configuration of the open-source help desk ticketing system "osTicket".

_<b>NOTE:</b> This demonstration uses materials created in the previous demonstration, ["Prerequisites and Installation"](https://github.com/terikaj/osticket-prereqs)._

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Microsoft Remote Desktop
- Internet Information Services (IIS)
- [osTicket Documentation](https://docs.osticket.com/en/latest/index.html)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)
- MacOS

<h2>Post-Install Configuration Objectives</h2>

- Create and Configure Roles
- Create and Configure Departments & Teams
- Create and Configure Agents (workers) & Users (clients)
- Configure SLA (Service-Level Agreements)
- Configure Help Desk Support Topics

<h2>Configuration Steps</h2>

<h3>&#9312; Prerequisites and Installation</h3>

_This demonstration assumes a virtual machine is established with  all prerequisite files installed for working osTicket._ </br>
_Credentials and configurations that will be used in this demonstration can be found in ["Prerequisites and Installation"](https://github.com/JTYKolesar/osticket-prereqs)._ </br>
<hr>

<h3>&#9313; Admin Panel - Roles, Departments, Teams, & Agents</h3>

- On the web browser (Microsoft Edge or Chrome), navigate to the Help Desk Login Page to sign into your osTicket Help Desk account (this example uses username **ostuser / ostuser@email.com**).
  - Help Desk Login Page -- http://localhost/osTicket/scp/login.php
<p align=center>
<img width="700" alt="Screen Shot 2024-04-05 at 3 37 53 PM" src="https://github.com/TerikaJ/post-install-config/assets/136477450/3e5c977d-0101-4478-9dec-97b790f3a9c2">
<img width="700" alt="Screen Shot 2024-04-05 at 3 39 08 PM" src="https://github.com/TerikaJ/post-install-config/assets/136477450/87c59a3c-5446-41d8-9194-390a5d798408">
</p>

- Click the "Admin Panel" button at the top-right of the page.
<p align=center>
<img width="700" alt="Screen Shot 2024-04-05 at 3 40 03 PM" src="https://github.com/TerikaJ/post-install-config/assets/136477450/588802ac-bfab-490f-bca3-b22ea1c9e63b">
</p>

- Click the "Agents" tab > "Roles" > "Add New Role".
<p align=center>
d<img width="700" alt="Screen Shot 2024-04-05 at 3 44 25 PM" src="https://github.com/TerikaJ/post-install-config/assets/136477450/3a31d524-d2f7-44b5-b9ac-93d498ee6c66">

</p>

_"Roles are the permissions granted to Agents via the Department they're responsible for."_
- In the "Definition" tab, type any "Role" name of your choice (this example uses **Supreme Admin**).
  - _This role will be given all permissions._
- Then, click the Permissions tab.
<p align=center>
<img width="700" alt="Screen Shot 2024-04-05 at 3 47 05 PM" src="https://github.com/TerikaJ/post-install-config/assets/136477450/f6fea620-99c1-4fc9-b16e-c21162bb3364">
</p>

- In the "Permissions" tab, under the "Tickets" category, checkmark ALL boxes.
  - Navigate through the Tasks and Knowledgebase categories and checkmark ALL boxes as well.
- Once done, click "Add Role".
<p align=center>
<img width="700" alt="Screen Shot 2024-04-05 at 3 49 46 PM" src="https://github.com/TerikaJ/post-install-config/assets/136477450/975b2744-19a2-4eab-bf9a-aeaf593e094e">
</p>

_Now we've created a Supreme Admin role with ALL permissions granted. Next, we'll create a Department._
- Currently in the "Agents" tab, click the "Departments" category.
- Click "Add New Department".
<p align=center>
<img width="700" alt="Screen Shot 2024-04-05 at 3 52 46 PM" src="https://github.com/TerikaJ/post-install-config/assets/136477450/f633bb70-66ed-4380-9813-6d4e608f592e">
</p>

- Create a Department name of your choice (this example uses **System Administrators**).
- Skip everything else and click "Create Dept".
<p align=center>
<img width="700" alt="Screen Shot 2024-04-05 at 3 55 01 PM" src="https://github.com/TerikaJ/post-install-config/assets/136477450/69aea382-d1a0-4ed9-8d00-764f701e3f63">
</p>

_Next, we'll move onto creating a Team._ <br>
_"Teams allow us to pull Agents from different Departments and organize them in order handle specific issues or user via a Help Topic, or through the Ticket Filter."_
- Currently in the "Agents" tab, click the "Teams" category.
- Click "Add New Team".
<p align=center>
<img width="700" alt="Screen Shot 2024-04-05 at 3 56 11 PM" src="https://github.com/TerikaJ/post-install-config/assets/136477450/f84ffc2a-97f2-4e05-ab2c-2d605ae69ce3">
</p>

- Create a Team name of your choice (this example uses **Level II Support**).
- Click "Create Team".
<p align=center>
<img width="903" alt="Screen Shot 2024-04-05 at 4 13 12 PM" src="https://github.com/TerikaJ/post-install-config/assets/136477450/43bbb965-9b34-4a6d-b16d-262113befec5">
</p>

- Currently in the "Agents" tab, click the "Agents" category.
<p align=center>
<img width="900" alt="Screen Shot 2024-04-05 at 4 14 19 PM" src="https://github.com/TerikaJ/post-install-config/assets/136477450/0db711c3-cba1-422d-8127-7c64c708fbcf">
</p>

- Create the required credentials for this user listed in bold:
  - First Name (this example uses **Jane**).
  - Last Name (this example uses **Doe**).
  - Email Address (this example uses **jane.doe@osTicket.com**).
  - Username (this example uses **jane.doe**).
- Click "Set Password" and a windows prompt will appear:
  -   Uncheck "Send the agent a password reset email".
  -   Create a password for this user.
  -   Uncheck "Require password change at next login".
  -   Click "Set".
<p align=center>
<img width="899" alt="Screen Shot 2024-04-05 at 4 16 51 PM" src="https://github.com/TerikaJ/post-install-config/assets/136477450/802bbaff-2bd2-4df4-9c2d-153fb11b55b8">
<img width="607" alt="Screen Shot 2024-04-05 at 4 19 31 PM" src="https://github.com/TerikaJ/post-install-config/assets/136477450/3f3ee42e-e7c2-49e4-b3cd-8e009b50a569">
</p>

- Click the "Access" tab:
  - Assign this user to the Department we created (this example uses **System Administrators**).
  - Assign this user to the Role that we created (this example uses **Supreme Admin**).
- Under "Extended Access", assign this user to the "Support" department with the "Supreme Admin" role.
- Click "Save Changes".
<p align=center>
<img width="902" alt="Screen Shot 2024-04-05 at 4 23 18 PM" src="https://github.com/TerikaJ/post-install-config/assets/136477450/131cac3d-9d34-48e1-9019-7433bcb4767f">
</p>

- Click on the "Teams" tab:
  -  Assign this user to the Team that we created (this example uses **Level II Support**).
-  Once done, click "Create".
<p align=center>
<img width="903" alt="Screen Shot 2024-04-05 at 4 26 02 PM" src="https://github.com/TerikaJ/post-install-config/assets/136477450/4d1e52ba-2873-4e29-84d6-1e074c00335d">
</p>

_Create a second Agent following the same steps, however, assign this agent to a different Role and Department._</br>
_This example creates Agent **"John Doe"** | Department: **"Level I Support"** | Role: **"View only** | Extended Access: **Support"**_.
<p align=center>
<img width="933" alt="Screen Shot 2024-04-05 at 4 30 07 PM" src="https://github.com/TerikaJ/post-install-config/assets/136477450/83860e77-4937-49e4-a583-249c0e9ccdd9">
<img width="903" alt="Screen Shot 2024-04-05 at 4 31 37 PM" src="https://github.com/TerikaJ/post-install-config/assets/136477450/f609d343-9bfd-4dcf-b665-8d26adcfe563">
</p>
<hr>

<h3>&#9314; Agent Panel - Creating Users</h3>

- Click "Agent Panel" at the top-right of the page.
<p align=center>
<img src="https://i.imgur.com/A6lRMQN.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Click the "Users" tab.
- Click "Add User".
- Create an Email Address and Full Name for this user (this example uses **karen@osticket.com / Karen Karen**).
- Click "Add User".
<p align=center>
<img width="750" alt="Screen Shot 2024-04-05 at 4 36 29 PM" src="https://github.com/TerikaJ/post-install-config/assets/136477450/da6a0afc-73a4-45c1-a272-f4a5745687c9">
<img width="750" alt="Screen Shot 2024-04-05 at 4 38 12 PM" src="https://github.com/TerikaJ/post-install-config/assets/136477450/9016113b-26d4-425a-9179-15546dba48ab">
</p>

_Create another user of your choice (this example uses **ken@osticket.com / Ken Ken**)_
<p align=center>
<img width="750" alt="Screen Shot 2024-04-05 at 4 40 43 PM" src="https://github.com/TerikaJ/post-install-config/assets/136477450/bacf31d0-b711-47c0-acc6-d4c9aa1c4892">
<img width="750" alt="Screen Shot 2024-04-05 at 4 41 49 PM" src="https://github.com/TerikaJ/post-install-config/assets/136477450/1b82dd37-5077-450d-828e-ba8000310eb9">
</p>
<hr>

<h3>&#9315; Admin Panel - Configuring SLA</h3>

_"SLA Plans or Service Level Agreements, are unlimited in osTicket. The purpose of the SLA is to provide a length of time in which the help desk Administrator should be expected to resolve and close the tickets."_
- Return to the "Admin Panel".
  - Navigate to the "Manage" tab > "SLA".
- Click "Add New SLA Plan".
<p align=center>
<img width="750" alt="Screen Shot 2024-04-05 at 4 43 02 PM" src="https://github.com/TerikaJ/post-install-config/assets/136477450/7e909d9b-0cb9-4fff-9e6b-ff0bf921018b">
</p>

- Create the following plans:
  - **SEV-A**
    - Grace Period: **1 hour** (_Amount, in hours, tickets with this SLA will become overdue if not closed in allotted time._)
    - Schedule: **24/7** (_Accounted for all days of the week, even on non-business days_)
  
  - **SEV-B**
    - Grace Period: **4 hours**
    - Schedule: **24/7**

  - **SEV-C**
    - Grace Period: **8 hours**
    - Schedule: **Monday - Friday 8am - 5pm with U.S. Holidays**
- Click "Add Plan" for each SLA.
<p align=center>
<img width="750" alt="Screen Shot 2024-04-05 at 4 48 00 PM" src="https://github.com/TerikaJ/post-install-config/assets/136477450/984fc86c-086d-4e57-b7e2-e94284424625">
<img width="750" alt="Screen Shot 2024-04-05 at 4 50 26 PM" src="https://github.com/TerikaJ/post-install-config/assets/136477450/87de32d6-f4dd-4ede-9f47-eba712c0a40b">
</p>
<hr>

<h3>&#9316; Configure Help Topics</h3>

_Help Topics will streamline our end-user’s help desk experience to ensure proper assignment and prompt response to the ticket._
- In the "Admin Panel", navigate to "Manage" tab > "Help Topics".
- Click "Add New Help Topic".
<p align=center>
<img width="750" alt="Screen Shot 2024-04-05 at 4 52 25 PM" src="https://github.com/TerikaJ/post-install-config/assets/136477450/42811d56-4081-40c3-8594-e8a27fefc075">
</p>

- Create Help Topics with the following names:
  - **Business Critical Outage**
  - **Personal Computer Issues**
  - **Equipment Request**
  - **Password Reset**
- "Internal Notes" can be written down for personal use, but are not necessary.
- Click "Add Topic".
<p align=center>
<img width="750" alt="Screen Shot 2024-04-05 at 4 55 14 PM" src="https://github.com/TerikaJ/post-install-config/assets/136477450/0124ee33-e2b0-49ef-9dd3-d605248899a1">
<img width="750" alt="Screen Shot 2024-04-05 at 4 58 35 PM" src="https://github.com/TerikaJ/post-install-config/assets/136477450/26c6f45d-150f-4c60-aa91-91bb4d1cd607">
</p>
<hr>

<h1><p align=center> DONE! Good job! </p></h1>

<h2><p align=center>The Next Demonstration:<br><a href="https://github.com/terikaj/ticket-lifecycle">Ticket Lifecycle Examples</a></p></h2>

<p align=right>Please delete & clean up your Azure resources when finished!<br>
If you're unsure of how to do this, please click <a href="https://github.com/terikaj/azure-begin">HERE</a>
</p>

