<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo" width="300"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Configure Roles (for grouping permissions)
- Configure Departments (Ticket Visibility, Help Desk vs SysAdmins, vs Networking)
- Configure Teams
- Allow anyone to create tickets
- Configure Agents (workers)
- Configure Users (customers)
- Configure SLA(Service Level Agreements)
- Configure Help Topics (For when users create a ticket)

## Configure Roles (for grouping permissions) 

I will create a new role for this section. Firstly, ensure that you are on the Admin Panel, select the Agents tab, and I will create a role named "Supreme Access," and assign all possible permissions(Tickets, Tasks, and Knowledgebases).

<p><strong>Creating new role - Supreme Access</strong></p>
<img src="https://github.com/user-attachments/assets/33a56e1b-501d-4698-b340-ffad8cce69d0" width="600"/>

<p><strong>Assigning permissions to role</strong></p>
<img src="https://github.com/user-attachments/assets/72a27bde-904d-4d1a-9a82-65d5d8a507a8" width="600"/>

## Configure Departments(Ticket Visibility, Help Desk vs SysAdmins, vs Networking)

For this portion, I will simply create a new department called "SysAdmin." Under "Parent", assign this department to the "Support" section, name it "Sysadmin", and complete the setup. 

Admin Panel --> Departments --> + Add New Department

<p><strong>Creating new department - SysAdmin</strong></p>
<img src="https://github.com/user-attachments/assets/b3e167b2-773a-4e7b-94bd-d6ca4918637f" width="600"/>

## Configure Teams

To configure Teams in osTicket, go to the Admin Panel> Agents> Teams. From there, create a new team and assign agents from different departments, such as Support or Online Banking. This allows you to group agents under a shared ticket queue, making it easier to collaborate and manage tickets across departments.

<p><strong>Teams tab in Admin Panel</strong></p>
<img src="https://github.com/user-attachments/assets/a0ef4d80-2270-454f-ad25-83def9ecc5c3" width="600"/>

<p><strong>Creating and assigning agents to a team</strong></p>
<img src="https://github.com/user-attachments/assets/4a2c47a2-d85a-4830-80f9-27cfbb39d464" width="600"/>

## Allow anyone to create tickets 

To allow anyone to create tickets in osTicket without requiring an account, navigate to Admin Panel> Settings> User Settings. Uncheck the option that says “Require registration and login to create tickets”. This will let unregistered users submit support requests, making it easier for first-time or external users to reach out. 

<p><strong>User Settings configuration</strong></p>
<img src="https://github.com/user-attachments/assets/007d6106-233f-4b31-aebd-c889de412e7b" width="600"/>

## Configure Agents(workers)

To manage customers in osTicket, you can configure users by navigating to the Agent Panel> Users> Add New. This section allows agents to manually add and manage customer profiles, such as creating entries for users like Karen and Ken. Setting up users ensures that tickets are properly associated with the right individuals, allowing for better tracking and a more complete support history. 

### User: Jane

<p><strong>Agent profile - Jane (1)</strong></p>
<img src="https://github.com/user-attachments/assets/b5c82e7e-2435-4db9-8727-413936a4a002" width="600"/>

<p><strong>Agent profile - Jane (2)</strong></p>
<img src="https://github.com/user-attachments/assets/59cf8be5-278c-44b1-9b62-a5bacc366fe8" width="600"/>

<p><strong>Agent profile - Jane (3)</strong></p>
<img src="https://github.com/user-attachments/assets/4ea54548-19b4-4d18-8864-39c78371fe00" width="600"/>

<p><strong>Agent profile - Jane (4)</strong></p>
<img src="https://github.com/user-attachments/assets/16c5e64c-dd9c-44b8-ab99-f0182f3d7b95" width="600"/>

### User: John 

<p><strong>Agent profile - John (1)</strong></p>
<img src="https://github.com/user-attachments/assets/5b47d302-0bb4-4d19-83f2-ef524b6a4209" width="600"/>

<p><strong>Agent profile - John (2)</strong></p>
<img src="https://github.com/user-attachments/assets/607f4b7e-38ed-4597-ad52-34ffc7539760" width="600"/>

<p><strong>Agent profile - John (3)</strong></p>
<img src="https://github.com/user-attachments/assets/10a0c77a-d4e6-43dd-a5e6-e5619ee4f84f" width="600"/>

<p><strong>Agent profile - John (4)</strong></p>
<img src="https://github.com/user-attachments/assets/799d08f1-3c88-4224-b221-e3d1e30893bf" width="600"/>

## Configure Users(customers)

To configure users (customers) in osTicket, go to the Agent Panel> Users> Add New. Here, you can manually create user profiles by entering details such as name and email, for example, by adding users named Karen and Ken. This helps link tickets to specific individuals, allowing agents to track communication and support history more effectively.

<p><strong>Customer profile - Karen & Ken</strong></p>
<img src="https://github.com/user-attachments/assets/2fdb5b87-ffc4-4c12-b589-e7f2ebf510da" width="600"/>

## Configure SLA(Service Level Agreements)

To configure SLAs (Service Level Agreements) in osTicket, navigate to Admin Panel → Manage → SLA. SLAs define the expected response or resolution time for tickets, helping ensure timely support based on priority. For example, you can set up:

Sev-A with a 1-hour grace period and a 24/7 schedule for critical issues,

Sev-B with a 4-hour grace period, also under a 24/7 schedule, and

Sev-C with an 8-hour grace period limited to Business Hours for lower-priority concerns.

These SLAs can then be assigned to departments or help topics to automate and enforce response timelines.

<p><strong>Sev-A SLA Configuration</strong></p>
<img src="https://github.com/user-attachments/assets/8e83143a-c9fa-468e-8603-2c822dc268f6" width="600"/>

<p><strong>Sev-B SLA Configuration</strong></p>
<img src="https://github.com/user-attachments/assets/1b01d74f-dbd0-435b-b485-7db25f9df5ed" width="600"/>

<p><strong>Sev-C SLA Configuration</strong></p>
<img src="https://github.com/user-attachments/assets/0ad567fc-9299-4daf-bbcf-82193f95f9a8" width="600"/>

<p><strong>All SLAs Overview</strong></p>
<img src="https://github.com/user-attachments/assets/a3fe079c-a80b-4bc8-b729-33ec59037cc3" width="600"/>

## Configure Help Topics(For when users create a ticket)

To configure Help Topics in osTicket, go to Admin Panel → Manage → Help Topics. Help Topics categorize incoming tickets, allowing you to tailor workflows, forms, and service-level agreements (SLAs) based on the nature of the request. For example, you can create topics such as Business Critical Outage, Personal Computer Issues, Equipment Request, Password Reset, and Other to automatically route tickets to the appropriate department or support team.

<p><strong>Help Topic Creation Panel</strong></p>
<img src="https://github.com/user-attachments/assets/aa1afbf2-8f1a-4792-a2e1-dd62d3ae5d7d" width="600"/>

<p><strong>Help Topic - Business Critical Outage</strong></p>
<img src="https://github.com/user-attachments/assets/40113161-e85c-4086-bbf6-dda24eea4cc2" width="600"/>

<p><strong>Help Topic - Equipment Request</strong></p>
<img src="https://github.com/user-attachments/assets/bf38751a-e1d0-4832-8a9c-2e5010d08ea0" width="600"/>

<p


















