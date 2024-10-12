# **Comprehensive osTicket Setup and Configuration Guide**

![osTicket Banner](https://github.com/KLavallais/KLavallais/blob/assets/osTicket%20Banner.png)

Welcome to the **osTicket Configuration Guide**, detailing how to set up roles, departments, teams, SLAs, agents, users, and help topics. The guide also touches on the separation between the **Agent Panel** and **Admin Panel** for specific tasks.

---

## **Table of Contents**
1. [Recognizing the Admin vs. Agent Panel](#recognizing-the-admin-vs-agent-panel)
2. [Configuring Roles](#configuring-roles)
3. [Configuring SLAs](#configuring-slas)
4. [Configuring Departments](#configuring-departments)
5. [Configuring Teams](#configuring-teams)
6. [Allowing Anyone to Create Tickets](#allowing-anyone-to-create-tickets)
7. [Configuring Agents](#configuring-agents)
8. [Configuring Users](#configuring-users)
9. [Configuring Help Topics](#configuring-help-topics)

---

## **1. Recognizing the Admin vs. Agent Panel**

Before diving into configuration, it’s important to distinguish between the **Admin Panel** and the **Agent Panel** in osTicket:

- **Admin Panel**: Used for system configuration, creating roles, managing departments, configuring SLAs, etc.
- **Agent Panel**: Used by agents for managing tickets, interacting with users, and managing day-to-day helpdesk tasks.

![Admin Panel Recognition](https://github.com/KLavallais/KLavallais/blob/assets/Recognizing%20Admin%20Panel.png)
![Agent Panel Recognition](https://github.com/KLavallais/KLavallais/blob/assets/Recognizing%20Agent%20Panel.png)

---

## **2. Configuring Roles**

Roles define what agents can do within osTicket. Set up roles for different levels of access and permissions.

**Path**: Admin Panel -> Agents -> Roles

Example: Creating the **Supreme Admin** role with full system permissions.

![Create Supreme Admin Role](https://github.com/KLavallais/KLavallais/blob/assets/Create%20Supreme%20Admin%20Role.png)

![Supreme Admin Permissions](https://github.com/KLavallais/KLavallais/blob/assets/Role%20Permissions.png)

![Successfully Added Role](https://github.com/KLavallais/KLavallais/blob/assets/Successfully%20Added%20Role.png)

---
## **3. Configuring SLAs**

Service Level Agreements (SLAs) define the time frames within which tickets should be handled based on severity.

**Path**: Admin Panel -> Manage -> SLA

- **Sev-A**: 1 hour, 24/7 schedule (Critical issues)
- **Sev-B**: 4 hours, 24/7 schedule (High priority)
- **Sev-C**: 8 hours, business hours schedule (Low priority)

Here’s an example of configuring **Sev-A**:

![SLA Plan Sev-A 01](https://github.com/KLavallais/KLavallais/blob/assets/SLA%20Plan%20Sev-A_0001.png)

![SLA Plan Sev-A 02](https://github.com/KLavallais/KLavallais/blob/assets/SLA%20Plan%20Sev-A_0002.png)

Similarly, **Sev-B** configuration:

![SLA Plan Sev-B](https://github.com/KLavallais/KLavallais/blob/assets/SLA%20Plan%20Sev-B.png)

And **Sev-C**:

![SLA Plan Sev-C](https://github.com/KLavallais/KLavallais/blob/assets/SLA%20Plan%20Sev-C.png)

---

## **4. Configuring Departments**

Departments allow you to organize tickets by areas of responsibility like Help Desk, SysAdmins, Networking, etc.

**Path**: Admin Panel -> Agents -> Departments

Create departments that will be visible to agents based on their responsibilities. Example: Setting up **SysAdmins**.

![Create SysAdmins Dept](https://github.com/KLavallais/KLavallais/blob/assets/Create%20SysAdmins%20Dept%20then%20choose%20SLA%20etc.png)

After setting up the department, here is the department list:

![SysAdmins Created Successfully](https://github.com/KLavallais/KLavallais/blob/assets/SysAdmins%20Created%20Successfully.png)

---

## **5. Configuring Teams**

Teams allow agents from different departments to collaborate on certain ticket categories. 

**Path**: Admin Panel -> Agents -> Teams

In this example, we configure a team called **Blue Team** to handle cross-departmental issues, such as tickets related to **Online Banking**.

![Create Blue Team](https://github.com/KLavallais/KLavallais/blob/assets/Create%20Blue%20Team.png)

Once configured, the team appears in the team list:

![Teams Configured](https://github.com/KLavallais/KLavallais/blob/assets/Team%20Creation%20Completed.png)

---

## **6. Allowing Anyone to Create Tickets**

By default, osTicket can allow or restrict ticket creation by unregistered users. To change this:

**Path**: Admin Panel -> Settings -> User Settings

- **UNCHECK**: Unregistered users can create tickets.
- **CHECK**: Registration required for users to create tickets.

![User Settings](https://github.com/KLavallais/KLavallais/blob/assets/System%20Settings%20and%20Preferences.png)

---

## **7. Configuring Agents**

Agents are responsible for managing and resolving tickets. Configure agents by assigning them to departments and roles.

**Path**: Admin Panel -> Agents -> Add New

- **Jane**: Assigned to **SysAdmins**.
- **John**: Assigned to **Support**.

Example: Adding **Jane Doe** as an agent.

![Create Agent Jane](https://github.com/KLavallais/KLavallais/blob/assets/Create%20Agent_0003.png)

Once added, assign the agent to their department (SysAdmins) and their role (Supreme Admin):

![Agent Access Configuration](https://github.com/KLavallais/KLavallais/blob/assets/Create%20Agent_0004.png)
![Agent Access Configuration](https://github.com/KLavallais/KLavallais/blob/assets/Create%20Agent_0005.png)

Assign specific permissions for the agent, such as managing user accounts:

![Configure Agent Permissions](https://github.com/KLavallais/KLavallais/blob/assets/Create%20Agent_0006.png)

Finally, assign the agent to a team, such as the **Blue Team**:

![Assign Agent to Team](https://github.com/KLavallais/KLavallais/blob/assets/Create%20Agent_0007.png)

---

## **8. Configuring Users**

Users are the customers who will submit tickets. They can be added manually or allowed to register through the user interface.

**Path**: Agent Panel -> Users -> Add New

- **Katie**: Added as a user for submitting tickets.
- **Kenny**: Another user added to the system.

Example: Adding **Katie Doe** as a user.

![Create User Katie](https://github.com/KLavallais/KLavallais/blob/assets/Create%20User_0003.png)

Once configured, Katie appears in the user directory.

![User Directory](https://github.com/KLavallais/KLavallais/blob/assets/Create%20User_0004.png)

---


## **9. Configuring Help Topics**

Help Topics guide users in selecting the correct category when submitting tickets, making it easier for agents to prioritize them.

**Path**: Admin Panel -> Manage -> Help Topics

Example topics include:
- **Business Critical Outage**
- **Personal Computer Issues**
- **Equipment Request**
- **Password Reset**

Here’s an example of adding a **Password Reset** help topic:

![Add Help Topic](https://github.com/KLavallais/KLavallais/blob/assets/Help%20Topics_0004.png)

Once added, the help topics appear in the list:

![Help Topics Configured](https://github.com/KLavallais/KLavallais/blob/assets/Help%20Topics_0005.png)

---

## **Conclusion**

This guide covers the complete configuration of osTicket, from roles and departments to SLAs and help topics. Follow these steps to ensure your helpdesk is efficiently organized and able to handle tickets with the appropriate response times and assignments.

Explore the images provided for visual guidance on each step of the setup.

--- 

By following these steps, you will have fully configured osTicket, ready for agents, users, and departments to function efficiently.

Feel free to clone or fork the repository to suit your organization’s needs.
