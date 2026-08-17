# LAB 08 — Branding & Site Design

## 🎯 Objective

Create a custom brand theme, build page templates, use Site Design templates for automated site provisioning, and use the SharePoint Look Book.

## 📋 Prerequisites

* SharePoint Admin Center access
* Site Owner role
* Optional: SharePoint Online Management Shell

---

## Task 8.1 — Create a Custom Theme

### 1. Open Theme Designer

Go to `aka.ms/spthemebuilder` → pick primary, secondary, and body text colours to match your brand.

### 2. Export the JSON

Click **Export** → copy the JSON theme object.

### 3. Apply to the tenant

**SharePoint Admin Center → Settings → Change the look → Themes → Add theme** → paste JSON → **Save**.

### 4. Apply to a site

**Site Settings → Change the look → Theme** → choose your custom theme → **Save**.

---

## Task 8.2 — Create Page Templates

### 1. Design a template page

Edit a page to your desired layout (header image, Quick Links, News, People web parts etc.).

### 2. Save as template

**Page details panel → Save as template** → give it a name and description.

### 3. Use the template

When creating a new page → choose **'From an existing template'** → select yours.

### 4. Manage templates

Templates are stored in **Site Pages library → Templates folder** — manage permissions there.

---

## Task 8.3 — Use Site Design Templates (Auto-provision Sites)

### 1. Create a Site Script (JSON)

Write a JSON site script defining lists, columns, themes, navigation to apply. Use PnP provisioning or SharePoint Online Management Shell.

### 2. Register the script

PowerShell:

```powershell
Add-SPOSiteScript -Title 'MyScript' -Content $script
```

→ note the script ID returned.

### 3. Create a Site Design

PowerShell:

```powershell
Add-SPOSiteDesign -Title 'HR Portal' -WebTemplate '68' -SiteScripts $scriptId
```

→ this appears in the site creation wizard.

### 4. Apply on new site creation

When creating a new site → choose the **Site Design** → all configurations are auto-applied.

---

## Task 8.4 — Use the SharePoint Look Book

### 1. Visit Look Book

Navigate to `lookbook.microsoft.com` → browse **Communication** and **Team site templates**.

### 2. Preview a template

Click any template → **Preview** to see the full design with web parts.

### 3. Add to tenant

Click **'Add to your tenant'** → sign in → choose a site → the template is provisioned automatically.

---

## 💡 Best Practice Tips

* 🎨 **Define corporate colours early:** Define corporate colours in Theme Builder before any site is created — retroactive rebranding is painful.
* 📐 **Centralise approved templates:** Store approved page templates in a **'Template'** site and restrict write access so layouts stay consistent.
* 🔐 **Restrict complex Site Designs:** Site Designs can be scoped to specific users/groups — restrict complex templates to SharePoint admins.
* ⚙️ **Use PnP PowerShell for advanced provisioning:** Use `pnp.github.io/powershell` for advanced site provisioning beyond Site Designs.
