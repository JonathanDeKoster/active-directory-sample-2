# On-Premises Active Directory Lab in Azure  

<p align="center">
  <img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo" width="200"/>
</p>

Deploy a fully functional **on-premises Active Directory environment** inside **Microsoft Azure**, complete with domain controllers, client machines, PowerShell automation, and Group Policy management.  

---

## **Table of Contents**  
1. [Overview](#overview)  
2. [Video Demonstrations](#video-demonstrations)  
3. [Technologies & Tools](#technologies--tools)  
4. [High-Level Steps](#high-level-steps)  
5. [Deployment & Configuration](#deployment--configuration)  
   - [Step 1: Prepare Azure Infrastructure](#step-1-prepare-azure-infrastructure)  
   - [Step 2: Deploy Active Directory](#step-2-deploy-active-directory)  
   - [Step 3: Automate User Creation](#step-3-automate-user-creation)  
   - [Step 4: Group Policy & Account Management](#step-4-group-policy--account-management)  
6. [Learning Outcomes](#learning-outcomes)  
7. [Code & Scripts](#code--scripts)  

---

## **Overview**  

This project demonstrates how to deploy an **Active Directory lab** in Azure:  

- Build a **Virtual Network** with VMs.  
- Deploy **Windows Server 2022** as a Domain Controller.  
- Join a **Windows 10 client** to the domain.  
- Automate user creation with **PowerShell**.  
- Manage accounts and security with **Group Policy**.  

---

## **Video Demonstrations**  

### Step 1: Preparing Active Directory  
[![Step 1: Preparing Active Directory](https://img.youtube.com/vi/LecWaZvwVhA/hqdefault.jpg)](https://youtu.be/LecWaZvwVhA)  

### Step 2: Deploying Active Directory  
[![Step 2: Deploying Active Directory](https://img.youtube.com/vi/P3ETSjE38Co/hqdefault.jpg)](https://youtu.be/P3ETSjE38Co)  

### Step 3: Creating Users  
[![Step 3: Creating Users](https://img.youtube.com/vi/9BPQEOOHzIU/hqdefault.jpg)](https://youtu.be/9BPQEOOHzIU)  

### Step 4: Group Policy Management  
[![Step 4: Group Policy Management](https://img.youtube.com/vi/u01zGACmFpI/hqdefault.jpg)](https://youtu.be/u01zGACmFpI)  

---

## **Technologies & Tools**  
- **Microsoft Azure** (VMs, Networking)  
- **Active Directory Domain Services (AD DS)**  
- **Group Policy Management**  
- **PowerShell Scripting**  
- **Remote Desktop Protocol (RDP)**  

### Operating Systems  
- **Windows Server 2022**  
- **Windows 10 (21H2)**  

---

## **High-Level Steps**  
1. Prepare Azure infrastructure (VMs, networking, IPs).  
2. Deploy and configure Active Directory Domain Services.  
3. Automate user creation with PowerShell.  
4. Configure and apply Group Policies.  

---

## **Deployment & Configuration**  

### **Step 1: Prepare Azure Infrastructure**  
- Create a **Virtual Network**.  
- Deploy 2 VMs:  
  - **DC-1 (Domain Controller)**  
  - **Client-1 (Windows 10 Client)**  
- Assign **static IP** to DC-1.  
- Configure **DNS** on Client-1 to point to DC-1.  
- Verify connectivity (`ping`, `ipconfig`).  

<details>
<summary>📸 Click to view Step 1 screenshots</summary>

<img width="1600" src="https://github.com/user-attachments/assets/d55772b5-487e-4cb0-acfe-c1ade1fe2298" />  

---

<img width="1600" src="https://github.com/user-attachments/assets/3dfa1612-4449-4f86-95ba-87b924cb2b47" />  

---

<img width="1600" src="https://github.com/user-attachments/assets/bd6f8a1c-9a38-48cd-8086-4e52bd1a7631" />  

---

<img width="1600" src="https://github.com/user-attachments/assets/24fa2734-a2e1-416f-8314-adfe52de0e5f" />  

---

<img width="1600" src="https://github.com/user-attachments/assets/060bacae-a942-4499-83eb-b498f42e66ca" />  

---

<img width="1600" src="https://github.com/user-attachments/assets/a6517164-d384-4a6d-882f-44ca272329b3" />  

---

<img width="1600" src="https://github.com/user-attachments/assets/23c9d5cd-1b7d-424b-9cdb-6765eaf298a1" />  

---

<img width="1600" src="https://github.com/user-attachments/assets/2019735b-1b48-42f4-a2b5-ec3e77d792c8" />  

</details> 


---

### **Step 2: Deploy Active Directory**  
- Install **AD DS** on DC-1.  
- Promote DC-1 as **Domain Controller** and create a new forest: `mydomain.com`.  
- Add admin user (**Jane Doe**).  
- Join Client-1 to the domain.  

<details>
<summary>📸 Click to view Step 2 screenshots</summary>

<img width="1600" src="https://github.com/user-attachments/assets/5ee9be30-733d-48ec-9f06-9015fffe9d38" />  

---

<img width="1600" src="https://github.com/user-attachments/assets/6888f45c-29e9-46f3-a149-eced6b29cc5a" />  

---

<img width="1600" src="https://github.com/user-attachments/assets/291f86d2-4081-433e-8f10-b31a1aa74bb6" />  

---

<img width="1600" src="https://github.com/user-attachments/assets/894bf2c8-733d-40c4-ad89-e47e59bcc14f" />  

---

<img width="1600" src="https://github.com/user-attachments/assets/dce8cb50-2e26-41e8-b4da-ad472b056b88" />  

---

<img width="1600" src="https://github.com/user-attachments/assets/9524fabb-980c-451d-98b5-54801c363585" />  

---

<img width="1600" src="https://github.com/user-attachments/assets/de0efa17-116a-419b-ba6f-8155c4cb942e" />  

</details>  



---


### **Step 3: Automate User Creation**  
- Add domain users to **Remote Desktop Users** group.  
- Run PowerShell script to bulk-create users.  
- Test login with sample user accounts.

<details>
<summary>📸 Click to view Step 3 screenshots</summary>

<img width="1600" src="https://github.com/user-attachments/assets/0a61881b-dd78-47ee-984c-0894681b19fd" />  

---

<img width="1600" src="https://github.com/user-attachments/assets/1b48f07b-c7f2-4eda-8733-28e03a03f716" />  

---

<img width="1600" src="https://github.com/user-attachments/assets/2206ac3d-3da2-4036-95c6-5d0302204d91" />  

---

<img width="1600" src="https://github.com/user-attachments/assets/c804a2f0-d4eb-4771-9557-6356f768134e" />  

</details>


---

### ***Step 4: Group Policy & Account Management***
- Configure Account Lockout Policy via gpmc.msc.

- Test user lockouts and resolutions.

- Enable/disable accounts in AD.

- Audit security logs in Event Viewer.

<details>
<summary>📸 Click to view Step 4 screenshots</summary>

<img width="1600" src="https://github.com/user-attachments/assets/34af0a1c-964d-4cb8-be65-8f18c8579f6c" /> 

---

<img width="1600" src="https://github.com/user-attachments/assets/050df9ef-987e-4a4a-aea2-6abe38043649" />  

---

<img width="1600" src="https://github.com/user-attachments/assets/4f8ac407-d5af-4910-80ca-00641995f28b" />  

---

<img width="1600" src="https://github.com/user-attachments/assets/192b9e7e-186c-441a-9ab0-10afb3e024c7" />  

---

<img width="1600" src="https://github.com/user-attachments/assets/368a787c-9b71-4c5d-a7d6-ef5a50b5bbb2" />  

---

<img width="1600" src="https://github.com/user-attachments/assets/4f1294b2-7252-4086-b64f-b825d06796d8" />  

</details>  


---



### ***Learning Outcomes***
- Built an Active Directory lab in Azure from scratch.

- Configured networking, DNS, and IP settings for domain environments.

- Automated user creation and management using PowerShell.

- Applied Group Policies for security and account management.

- Gained hands-on experience troubleshooting AD logs and security events.


