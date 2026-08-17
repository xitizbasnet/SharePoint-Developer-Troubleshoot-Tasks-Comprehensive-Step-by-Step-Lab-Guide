# LAB 02 — Document Sharing & Collaboration

## 🎯 Objective

Share documents with people inside and outside your organisation, manage co-authoring, and control sharing links.

## 📋 Prerequisites

* SharePoint site with a Document Library
* File(s) to share
* Tenant sharing settings enabled

---

## Task 2.1 — Share a Document Internally

### 1. Open the document library

Navigate to the **Library** → hover over the file → click the **'...' (ellipsis)** → **Share**.

### 2. Choose sharing scope

In the **Share** dialog, select **'People in [Your Organisation]'** from the link settings dropdown.

### 3. Set permission

Toggle between **Can Edit / Can View / Can Comment** based on the recipient's role.

### 4. Add recipients & send

Type names or email addresses → optionally add a message → click **Send**.

---

## Task 2.2 — Share a Document Externally (Guest Access)

> ⚠️ **Note:** External sharing must be enabled by your SharePoint/Global Admin first (**SharePoint Admin Center → Policies → Sharing**).

### 1. Open Share dialog

Select the file → **Share** → click the **link settings gear** → choose **'Specific people'**.

### 2. Enter external email

Type the guest's email address. SharePoint sends them an invite with a magic link.

### 3. Set expiry (recommended)

Set a link expiration date (e.g., **30 days**) so access doesn't remain indefinitely.

### 4. Verify guest access

Go to **Site Settings → Site Permissions** → check the guest appears under **'Site Visitors'**.

---

## Task 2.3 — Give Read vs Edit Access (Mixed Permissions)

### 1. Break inheritance on the item

**File** → **'...'** → **Manage Access** → **Advanced** → **Stop Inheriting Permissions**.

### 2. Remove unwanted groups

Remove inherited groups that should not have access to this specific file.

### 3. Grant specific users read

**Grant** → enter name → choose **Read** → **OK**.

### 4. Grant other users edit

**Grant** → enter name → choose **Edit (or Contribute)** → **OK**.

---

## 💡 Best Practice Tips

* 📁 **Prefer library or folder-level sharing:** Share at the library or folder level rather than file-by-file to reduce management overhead.
* 🔗 **Limit 'Anyone with the link':** Use this option sparingly. Prefer **'Specific people'** for sensitive documents.
* ⏳ **Set link expiry dates:** Always set expiration dates for external shares.
* 🛡️ **Enable sensitivity labels:** Use **Microsoft Purview** sensitivity labels to automatically apply sharing restrictions to classified documents.
* 🔍 **Regularly review sharing:** Review sharing through **Reports → Sharing** in the SharePoint Admin Center.
