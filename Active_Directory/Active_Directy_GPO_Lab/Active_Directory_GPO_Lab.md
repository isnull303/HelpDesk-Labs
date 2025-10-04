# Active Directory GPO Lab

## Overview  
In this lab, I practiced Group Policy Object (GPO) management within Active Directory.
The tasks focused on:
- Restricting Control Panel access
- Configuring an auto-lock screen policy
- Allowing local logon for domain users

These exercises helped me understand how GPOs are created, edited, linked to Organizational Units (OUs), and tested with domain accounts to control system behavior and access policies.

## Steps and Screenshots  

### Task 1: Restricting Control Panel Access  

- I created a new GPO named **Restrict Control Panel Access**. 

![](./screenshots/Restrict_Control_Panel_Access.png)  

- Edited the GPO to configure **Prohibit access to Control Panel and PC settings** (Enabled the restriction policy).
  
![](./screenshots/Prohibit_Access_Is_Enabled.png)  

- Linked the GPO to **Management, Marketing, and Sales OUs**. 

![](./screenshots/GPO_Linked.png)  

### Task 2: Configuring Auto-Lock Screen Policy 

- Created a new GPO named **Auto Lock Screen**. 

![](./screenshots/GPO_Auto_Lock_Screen.png)  

- Linked it to the **Root Domain**.  

![](./screenshots/Linked_To_The_Root_Domain.png)  

- Configured the **Machine Inactivity Limit** to 600 seconds (10 minutes). 

![](./screenshots/Inactivity_Limit.png)  

### Task 3: Allowing Local Logon for Domain Users

> To allow domain users to log in locally, added the user integrity to Account Operators or another group with local login rights.

![](./screenshots/Allow_log_on_locally.png)  

### Task 4: Testing the Policies  

- Used the domain user **integrity** in the **Marketing OU** for testing.

![](./screenshots/Marketing_User.png)  

- Logged in to the server VM as integrity. 

![](./screenshots/Sigining_In.png)  

- Attempted to open Control Panel – restriction worked as expected. 

![](./screenshots/Control_Panel_Restrictions_Error.png)  

- Waited for 5 minutes – user session logged out automatically.  

![](./screenshots/Got_Logged_Out.png)  


## Conclusion  

This lab demonstrated how to create, configure, and apply Group Policy Objects in an Active Directory environment.
I successfully implemented:
- Control Panel restriction
- Auto-lock after inactivity
- Local logon permissions

By linking these GPOs to the appropriate OUs and testing them with domain users, I gained hands-on experience in managing both security and access policies within Active Directory.
