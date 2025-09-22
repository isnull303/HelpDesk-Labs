# Windows Administration Lab: Local Group Policy for Security

## Overview
This lab demonstrates how to **secure a Windows 10 endpoint using Local Group Policy** by enforcing password complexity requirements and disabling USB storage devices. These are essential steps in hardening a system to prevent weak credentials and unauthorized data access.

---

## Steps and Screenshots

### 1. Accessing the Local Group Policy Editor; Enforce Password Complexity

1. Navigate to:  
**Computer Configuration → Windows Settings → Security Settings → Account Policies → Password Policy**

2. Enable **Password must meet complexity requirements**.  

![](./screenshots/Password_Complexity_Requirements.png)  

3. I have set **Minimum Password Length** to **8 characters**.  

![](./screenshots/Minimum_Password_Length.png) 

---

### 2. Disable USB Storage Devices

1. Navigate to:  
**Computer Configuration → Administrative Templates → System → Removable Storage Access**

2. External storage policy is implemented by enabling **All Removable Storage classes: Deny all access**.  

![USB Storage Denied Policy](./screenshots/All_Removable_Storage_Classes.png)

---

### Step 4: Verify the Policy

1. Policies are applied immediately by running **gpupdate/force** in **Command Prompt**

![Policy Updated](./screenshots/Policy_Updated_CMD.png) 

2. I tested **Password policy** by setting a weak password and it failed. 

![Password Failed](./screenshots/Password_Failed.png) 

3. Lastly, I tested **Removable Storage Policy** by plugging a USB drive. Access was denied.

![USB Access Denied](./screenshots/USB_Access_Denied.png)

---

## Conclusion
This lab successfully demonstrated **Windows Group Policy Implementation**. I:

- Enforced **Password Complexity** and minimum length requirements for stronger authentication.  
- Disabled **USB storage devices** to prevent unauthorized data access.  
- Verified applied policies to ensure endpoint security hardening is effective.  
