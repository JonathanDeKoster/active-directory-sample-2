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
<img width="1600" src="https://github.com/user-attachments/assets/
