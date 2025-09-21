# Lab 01 – Local User Account Management in Windows 11

## Overview
This lab demonstrates how to perform common user account management tasks in Windows 10:
- Create and delete local user accounts
- Reset user passwords
- Add users to local groups
- Verify changes using Command Prompt

These are typical real-world tasks performed by Help Desk and Junior System Administrators.

---

## Steps & Screenshots

### 1. Create a New Local User Accounts
- Open **Local Users and Groups (lusrmgr.msc)** → **Users → New User…**  
- Created user: **emma** > (my future wife)
- Created user: **void**
- Assigned initial passwords for both users
 
![](./screenshots/emma_User_Account_Setup.png)  
![](./screenshots/void_User_Account_Setup.png.png)  

---

### 2. Add User to Local Groups
- **emma** → Open Properties → **Member Of tab** → Added to **Administrators** group (she controls it all 💖)
- **void** → Open Properties → **Member Of tab** → Added to Remote Desktop Users group 
 
![](./screenshots/Admin_Added_To_Local_Group.png) 
![](./screenshots/Admin_Group_Membership.png) 
![](./screenshots/User_Added_To_Group_Membership.png)  
![](./screenshots/User_Group_Membership.png)  

---

### 3. Reset a User Password
- Right-clicked user **void** → **Set Password** → entered new password.  
 
![Password Reset Confirmation](./screenshots/Password_Reset_Confirmation.png)  

---

### 4. Delete an Old User Account
- Right-clicked **old user** account → **Delete** → Confirmed deletion.  
 
![User Deletion Confirmation](./screenshots/Confirmation_Of_User_Deletion.png)  

---

### 5. Verify Using Command Prompt
- Ran `net user` before and after deletion to verify user list.  

![Users List Before](./screenshots/Users_List.png)  
![Updated Users List](./screenshots/Updated_Users_List.png)  

---

## Conclusion
This lab successfully demonstrated how to:  

- Create a new user account  
- Reset a user password  
- Add a user to local groups  
- Delete an obsolete account  
- Verify changes with Command Prompt  

These are essential skills for IT Support/Help Desk technicians to manage local accounts in a Windows environment.
