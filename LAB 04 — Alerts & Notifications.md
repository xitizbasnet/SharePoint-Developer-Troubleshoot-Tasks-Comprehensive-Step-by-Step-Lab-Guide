# LAB 04 — Alerts & Notifications

## 🎯 Objective

Configure alerts so you are notified by email or SMS when documents are updated or deleted.

## 📋 Prerequisites

* SharePoint site
* Document Library
* Valid email address set in M365 profile

---

## Task 4.1 — Alert When Someone Updates a Document

### 1. Open the library

Navigate to the **Document Library** containing the files you want to monitor.

### 2. Open Alert Me

**Library toolbar** → **'...' More** → **Alert Me**, OR select a specific file → **'...'** → **Alert Me**.

### 3. Configure alert settings

Set:

* **Alert Title**
* **Delivery method:** Email/SMS
* **When to send:** Anything changes / Someone else changes / Item is modified

### 4. Set frequency

Choose:

* **Immediately**
* **Daily summary**
* **Weekly summary**

→ Click **OK**.

### 5. Test the alert

Edit a document → verify you receive the email notification.

---

## Task 4.2 — Alert When Someone Deletes a Document

### 1. Create a deletion alert

Go to the library → **'...'** → **Alert Me** → **New Alert**.

### 2. Change When to send alert

Under **'Send Alerts for These Changes'**, select **'Items are deleted'**.

### 3. Save and test

Click **OK** → delete a test file → confirm the email arrives.

### 4. Use Power Automate for advanced alerts

SharePoint trigger: **'When a file is deleted'** → send email/Teams message with file name and deleted-by info.

---

## 💡 Best Practice Tips

* ⚙️ **Use Power Automate for richer notifications:** Include the file name, modified-by information, and a direct link in notifications.
* 📬 **Avoid excessive immediate alerts:** Do not set alerts to **'Immediately'** on busy libraries. Use **'Daily summary'** to prevent inbox flooding.
* 🧹 **Manage your alerts:** Go to **Site Settings → My Alerts** to delete stale alerts.
* 🛡️ **Alert critical stakeholders:** For critical compliance libraries, alert the **site owner AND compliance officer** simultaneously using Power Automate.
