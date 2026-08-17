# LAB 11 — Microsoft Forms & Embedding

## 🎯 Objective

Embed a Microsoft Form on a SharePoint page to collect feedback, and use the Embed web part to display external websites.

## 📋 Prerequisites

* Microsoft Forms access (M365 licence)
* SharePoint page editing rights
* Internet accessible target URL

---

## Task 11.1 — Embed a Microsoft Form on a Page

### 1. Create the Form

Go to `forms.office.com` → **+ New Form** → add questions (**Choice, Text, Rating, Date**).

### 2. Get the embed code

**Form → '...' → Embed** → copy the full HTML code.

### 3. Add to SharePoint page

**Edit page → '+' → Microsoft Forms web part** → paste the form URL in the web part config, OR use **Embed web part** and paste the iframe.

### 4. Configure response settings

In Microsoft Forms → **Responses** → toggle:

* **'Record name'**
* **'One response per person'**
* **'Accept responses'**

### 5. View responses

**Microsoft Forms → Responses tab → Open in Excel** for analysis, or connect to Power BI.

---

## Task 11.2 — Embed an External Website in a SharePoint Page

### 1. Edit the page

Navigate to the SharePoint page → click **Edit**.

### 2. Add Embed web part

**'+' → search 'Embed' → select**.

### 3. Enter the URL or code

In the web part properties panel → paste the website URL or iframe embed code.

### 4. Check X-Frame-Options

Not all websites allow embedding. If blank/error, the target site blocks iframes. Use a proxy or check with your IT team.

### 5. Resize and publish

Adjust the web part height in properties → **Republish**.

---

## 💡 Best Practice Tips

* 🏢 **Keep organisational data within Microsoft 365:** Use Microsoft Forms instead of Google Forms to keep data within your Microsoft 365 tenant boundary.
* 🔐 **Restrict internal feedback when appropriate:** Limit form responses to **'People in my organisation only'** for internal feedback.
* 🌐 **Verify iframe support:** External websites must allow iframe embedding (no `X-Frame-Options: DENY/SAMEORIGIN` header) — check with the site owner.
* 🔄 **Automate response tracking:** Connect Forms responses directly to a SharePoint List via Power Automate for automatic tracking.
