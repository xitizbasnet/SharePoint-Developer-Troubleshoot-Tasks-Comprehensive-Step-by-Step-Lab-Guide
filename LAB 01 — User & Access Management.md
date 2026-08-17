# LAB 01 — User & Access Management

## Objective

Create and manage SharePoint accounts, users, groups, folders, files, and sites.

## Prerequisites

* Microsoft 365 admin account
* SharePoint admin role
* Modern browser

## Overview

SharePoint administration starts with understanding how identities, groups, and permissions interlock. This lab walks through creating accounts in M365, organising users into security groups, and then wiring those groups to SharePoint site permissions.

---

## Task 1.1 — Create a User Account

### 1. Open Microsoft 365 Admin Center

Navigate to `admin.microsoft.com` → **Users** → **Active Users** → **Add a user**.

### 2. Fill in user details

Enter **Display Name**, **Username (UPN)**, and assign a Microsoft 365 license (e.g., E3/E5).

### 3. Set password options

Choose auto-generate or set manually. Optionally require password change on first login.

### 4. Assign roles

Keep **'No admin access'** for standard users or assign **'SharePoint Administrator'** if needed.

### 5. Save and communicate

Click **Finish adding** → note the temp password → send login details securely to the user.

---

## Task 1.2 — Create SharePoint Groups

### 1. Go to Site Permissions

Open your SharePoint site → **Settings (⚙)** → **Site Permissions** → **Advanced Permission Settings**.

### 2. Create a new group

Click **'Create Group'** → give it a meaningful name (e.g., **'HR Team Members'**) → set permissions.

### 3. Add members

Under **Group Membership**, click **'New'** → type names or emails → click **Share**.

### 4. Assign permission level

Choose **Read**, **Contribute**, **Edit**, or **Full Control**. Follow least-privilege principles.

---

## Task 1.3 — Create Sites, Folders & Files

### 1. Create a Team or Communication site

**SharePoint home** → **+ Create site** → choose **Team Site** or **Communication Site** → fill details.

### 2. Add a Document Library

**Site contents** → **+ New** → **Document Library** → give name → **Create**.

### 3. Create folders

Inside the library → **+ New** → **Folder** → name it by project, department, or date.

### 4. Upload files

Drag-and-drop from Explorer into the library, or use **Upload** → **Files / Folder**.

---

## 💡 Best Practice Tips

>  Always create M365 Groups or Security Groups at the Azure AD level — avoid managing individuals directly on site permissions.

>  Use 'Unique Permissions' on sub-folders sparingly; inheritance is easier to audit.

>  Name groups consistently: [Site]-Owners, [Site]-Members, [Site]-Visitors.

>  Document all permission changes in a central log list for governance audits.

>  Enable MFA (Multi-Factor Authentication) for all users before granting SharePoint access.**

---

