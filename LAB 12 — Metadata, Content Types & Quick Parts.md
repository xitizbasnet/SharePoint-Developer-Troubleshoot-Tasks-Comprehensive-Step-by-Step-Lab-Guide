# LAB 12 — Metadata, Content Types & Quick Parts

## 🎯 Objective

Use Content Types to manage metadata at scale, set calculated default values, use Quick Parts in Office documents, and create dynamic pages with filters.

## 📋 Prerequisites

* Site Collection Admin
* SharePoint Content Type Hub (optional)
* Office 365 desktop apps

---

## Task 12.1 — Use Content Types to Manage Metadata

### 1. Open Content Type Hub or Site

**Site Settings → Site Content Types → Create** → choose **Parent Content Type → Document**.

### 2. Add columns (site columns)

Inside the content type → **Add from new site column** → define:

* **Name**
* **Type**
* **Default**
* **Required**

### 3. Add to a library

**Library Settings → Content Types → Add from existing site content types** → select yours.

### 4. Set as default

In the library content type list, click **'Change new button order'** → move yours to position 1.

---

## Task 12.2 — Set Default Metadata Values Using Calculations

### 1. Add a Calculated column

**Library Settings → Create column** → type: **Calculated** → enter formula (e.g., `=TEXT(TODAY(),"YYYY-MM")`).

### 2. Use Column Default Value Settings

**Library → Library Settings → Column default value settings** → set static or calculated defaults per folder.

### 3. Use metadata navigation

Enable library metadata navigation for large libraries:

**Library Settings → Metadata navigation settings**.

---

## Task 12.3 — Link Document Templates to the Library New Button

### 1. Upload a template

**Library Settings → Advanced Settings → Document Template** → upload your `.dotx` or `.xlsx` template, OR go to the **Forms** folder in the library and upload there.

### 2. Associate with Content Type

**Content Type in the library → Advanced Settings → Document Template** → enter or browse to the template URL.

### 3. Test

Click **+ New** in the library → the content type should open a new document pre-filled with the template.

---

## Task 12.4 — Use Quick Parts to Inject SharePoint Metadata into Office Docs

### 1. Open document from SharePoint

Open a Word document stored in a SharePoint library in the desktop Word app.

### 2. Insert Quick Part

**Word → Insert → Quick Parts → Document Property** → select a SharePoint column (e.g., **Project Name**).

### 3. The field is auto-populated

The field pulls the value from the library column metadata and renders it inside the document.

### 4. Save back to SharePoint

**Save** → the metadata and the document content remain in sync.

---

## 💡 Best Practice Tips

* 🏗️ **Create reusable site columns:** Create site columns at the **Site Collection** level, not inside individual libraries, to reuse them across sites.
* 🌐 **Publish Content Types centrally:** Publish Content Types to the **Content Type Hub (`admin.microsoft.com`)** to share them across site collections.
* 🧩 **Keep Content Types manageable:** Avoid creating more than **20 content types per library** to keep the **'New'** menu manageable.
* 🧮 **Test calculated formulas:** Calculated columns use Excel-style formulas — test your formula in Excel before adding it to SharePoint.
