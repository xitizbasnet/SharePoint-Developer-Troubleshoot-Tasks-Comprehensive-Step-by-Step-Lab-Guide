# LAB 05 — Navigation & Site Architecture

## 🎯 Objective

Configure Quick Links, create a mega menu, connect sites to a Hub, and display dynamic site lists.

## 📋 Prerequisites

* SharePoint site
* Hub site registered (for hub tasks)
* Site Owner permissions

---

## Task 5.1 — Use Quick Links to Navigate to Other URLs

### 1. Edit the page

Click the **Edit** button (pencil icon) on any modern SharePoint page.

### 2. Add Quick Links web part

Click **'+'** → search **'Quick links'** → select the web part.

### 3. Add links

Click **'+ Add'** inside the web part → enter URL and display name → optionally pick an icon.

### 4. Choose layout

Select **Button, Compact, Grid, Filmstrip, or List** layout from the web part toolbar.

### 5. Publish

Click **Republish** to make changes visible to all users.

---

## Task 5.2 — Create a Mega Menu

### 1. Open Navigation settings

**Site Settings → Navigation** OR click **'Edit'** on the top nav bar of a modern site.

### 2. Add top-level items

Click **'+ Add link'** → type the link label and URL for the main menu category.

### 3. Add sub-items (mega menu)

Hover over the top-level item → click **'...'** → **Add sub-link**. Repeat for all sub-items.

### 4. Organise columns

Drag sub-links into separate columns within the mega menu flyout for clean organisation.

### 5. Save

Click **Save**. Test the menu on both desktop and mobile views.

---

## Task 5.3 — Connect Sites to a Hub (Hub Site)

### 1. Register a Hub site

**SharePoint Admin Center → Sites → Active Sites** → select the site → **Hub → Register as hub site**.

### 2. Associate sites to the Hub

On each child site → **Settings → Site Information → Hub site association** → choose your Hub.

### 3. Verify shared navigation

Hub navigation and theme now automatically apply to all associated sites.

### 4. Display dynamic site list

Add the **'Sites'** web part on the Hub home page — it auto-lists sites the current user follows or belongs to.

---

## 💡 Best Practice Tips

* 🗺️ **Plan your information architecture (IA):** Plan your information architecture before creating Hub sites to avoid re-registering later.
* 🧭 **Keep mega menus manageable:** Limit the top-navigation mega menu to **2 levels** and approximately **7 items per column** for usability.
* 🔄 **Use dynamic content when appropriate:** Use the **'Highlighted content'** web part instead of a static Quick Links list for dynamic content.
* ⚠️ **Use Hub navigation carefully:** Hub sites propagate navigation changes to all associated sites. Use this feature with care on large tenants.
