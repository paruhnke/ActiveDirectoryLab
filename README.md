# 🏠 Active Directory Home Lab

## 📌 Overview

This project is a **Windows Active Directory home lab** designed to simulate a small enterprise network environment. The lab demonstrates core **system administration, identity management, and security fundamentals** using Microsoft Active Directory.

It is intended for **learning, practice, and portfolio demonstration** purposes.

---

## 🎯 Objectives

* Deploy and configure **Active Directory Domain Services (AD DS)**
* Create and manage **users, groups, and organizational units**
* Implement **Group Policy Objects (GPOs)**
* Join client machines to a domain
* Practice basic **IT administration and troubleshooting**
* Understand enterprise-style **authentication and authorization**

---

## 🧰 Technologies Used

* **Windows Server 2019 / 2022**
* **Windows 10 / 11**
* **Active Directory Domain Services**
* **Group Policy Management**
* **DNS**
* **PowerShell**
* **VirtualBox / VMware**

---

## 🖥️ Lab Architecture

| Machine  | OS             | Role                      |
| -------- | -------------- | ------------------------- |
| DC01     | Windows Server | Domain Controller, DNS    |
| CLIENT01 | Windows 10/11  | Domain-joined workstation |

**Domain Name:** `homelab.local`
**Network Type:** Internal / NAT

---

## ⚙️ Setup Steps

### 1️⃣ Create Virtual Machines

* Install Windows Server on **DC01**
* Install Windows 10/11 on **CLIENT01**
* Configure network adapter to **Internal Network** or **NAT**

---

### 2️⃣ Configure Domain Controller

* Set static IP address
* Install **Active Directory Domain Services**
* Promote server to **Domain Controller**
* Create new forest: `homelab.local`
* Verify DNS functionality

---

### 3️⃣ Active Directory Configuration

* Create Organizational Units:

  * `Users`
  * `Computers`
  * `IT`
  * `HR`
* Create user accounts and security groups
* Assign users to groups

---

### 4️⃣ Group Policy Implementation

* Create and link GPOs:

  * Password policy enforcement
  * Desktop restrictions
  * Drive mapping
  * Login banner
* Test policy application using `gpupdate /force`

---

### 5️⃣ Domain Join Client Machine

* Join **CLIENT01** to `homelab.local`
* Log in with domain user account
* Verify GPO application

---

## 🔐 Security Concepts Practiced

* Centralized authentication
* Least privilege access
* Group-based permissions
* Password policies
* User account management

---

## 🧪 Validation & Testing

* Domain user login success
* GPO enforcement confirmed
* DNS name resolution working
* Group permissions applied correctly

---

## 📚 Skills Demonstrated

* Windows Server administration
* Active Directory management
* Identity & Access Management (IAM)
* Networking fundamentals
* Troubleshooting and documentation

---

## 📸 Screenshots (Optional)

* Active Directory Users and Computers
* Group Policy Management Console
* Domain-joined client machine

---

## 🚀 Future Improvements

* Add File Server with NTFS permissions
* Implement DHCP
* Configure RDP access policies
* Add PowerShell automation scripts
* Integrate Azure AD (Hybrid setup)
