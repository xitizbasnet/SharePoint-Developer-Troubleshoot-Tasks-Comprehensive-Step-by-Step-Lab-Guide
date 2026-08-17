# LAB 06 — Security & Access Control

## 🎯 Objective

Create secure private channels, apply audience targeting, and show or hide content based on user attributes.

## 📋 Prerequisites

* SharePoint site
* Site Owner or Admin role
* M365 Groups and Entra ID groups configured

---

## Task 6.1 — Create a Secure Location (Limited Access)

### 1. Create a new Document Library

**Site Contents → + New → Document Library** → name it (e.g., **'HR Confidential'**).

### 2. Break permission inheritance

**Library Settings → Permissions for this document library → Stop Inheriting Permissions**.

### 3. Remove default groups

Delete **'Members'** and **'Visitors'** from the permission list, leaving only **'Owners'** and the restricted group.

### 4. Add restricted users/group

**Grant Permissions** → enter the restricted group name → assign **Contribute** or **Read**.

### 5. Test access

Log in as a non-member user and confirm they receive **'Access Denied'**.

---

## Task 6.2 — Show or Hide Content Based on Audience

### 1. Enable audience targeting

For a list/library: **Library Settings → Audience targeting settings → Enable → OK**.

### 2. Target a web part

**Edit page** → select the web part → **web part settings → Audience targeting → Add a group**.

### 3. Target a navigation item

**Edit navigation** → select a link → **Audience → choose an M365 group**.

### 4. Test as different user

Use a browser in **Private/InPrivate** mode logged in as a different user to verify visibility.

---

## 💡 Best Practice Tips

* 🛡️ **Audience targeting is not security:** Audience targeting **does not replace permissions** — users can still access content if they have the URL.
* 🔐 **Combine targeting with permissions:** Use audience targeting for personalised display and broken permission inheritance for true security.
* 👥 **Use M365 Groups:** Use **M365 Groups**, rather than security groups, for audience targeting in modern SharePoint.
* 🔍 **Audit permissions regularly:** Audit permission changes monthly using **SharePoint Admin Center → Reports → Access requests**.
* ⏱️ **Use Privileged Identity Management:** Consider using **Azure AD Privileged Identity Management (PIM)** for just-in-time admin access.
