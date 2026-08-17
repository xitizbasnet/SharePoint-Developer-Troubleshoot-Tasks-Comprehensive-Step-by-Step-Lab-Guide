# LAB 10 — Power Platform Integration

## 🎯 Objective

Build automated business processes using Power Automate, embed Power BI reports, and use SharePoint Lists as a data source for Power Apps.

## 📋 Prerequisites

* Power Automate licence
* Power BI Pro/Premium
* SharePoint List with data
* Power Apps licence

---

## Task 10.1 — Create Business Processes with Power Automate + SharePoint

### 1. Open Power Automate

Go to `make.powerautomate.com` → **+ Create** → **Automated cloud flow**.

### 2. Set SharePoint trigger

Choose trigger: **'When an item is created or modified'** → select **Site URL** and **List name**.

### 3. Add actions

Add steps:

* **'Send an email (V2)'**
* **'Post a message in Teams'**
* **'Create item in another list'**
* **'Start an approval'**

### 4. Test the flow

**Save → Test → manually** → create/update a list item → verify the flow runs successfully.

### 5. Embed flow button on a page

**Edit SP page → add 'Power Automate' web part** → configure to show a flow trigger button.

---

## Task 10.2 — Insert Power BI Reports into SharePoint Pages

### 1. Publish to Power BI service

In **Power BI Desktop → File → Publish** → choose your workspace.

### 2. Get embed URL

In **Power BI service → report → File → Embed report → SharePoint Online** → copy the URL.

### 3. Add Power BI web part

**Edit SharePoint page → '+' → Power BI** → paste the embed URL → configure report page and filter.

### 4. Publish the page

The report renders interactively for all users who have Power BI access.

---

## Task 10.3 — Use SharePoint Lists as Data Source for Power Apps

### 1. Create the List

Design your SharePoint list with all needed columns (the data model for your app).

### 2. Open Power Apps

From the list toolbar → **Integrate → Power Apps → Create an app** (auto-generates a canvas app).

### 3. Customise the app

In **Power Apps Studio** → modify **Browse, Detail, and Edit** screens to match your UI needs.

### 4. Save & Publish

**File → Save → Publish** → share the app with users via their **Azure AD group**.

### 5. Embed the app in SharePoint

**Edit SP page → '+' → Power Apps web part** → paste the app web link.

---

## 💡 Best Practice Tips

* 🗃️ **Choose the right data platform:** Use **Dataverse for Teams** for complex multi-table apps — SharePoint Lists work well for simple flat data.
* 🛡️ **Implement Power Automate error handling:** Apply flow error handling (**Configure run after → has failed**) to avoid silent failures.
* 📊 **Use Power BI URL filtering:** Filter Power BI embeds using URL parameters to show context-relevant data to site visitors.
* 🔐 **Use scalable permissions:** Grant Power Apps permissions at the **SharePoint List level**, not individual items, for scalable access control.
