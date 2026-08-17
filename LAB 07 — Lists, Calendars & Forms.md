# LAB 07 — Lists, Calendars & Forms

## 🎯 Objective

Build SharePoint Lists as data sources, add calendar views, create forms for processes, and use JSON column formatting.

## 📋 Prerequisites

* SharePoint site
* Member or Owner permissions
* Power Automate licence (for automated forms)

---

## Task 7.1 — Create a SharePoint List

### 1. Create the list

**Site Contents → + New → List** → choose **Blank list** or a built-in template (**Tasks, Issue Tracker**) → name it.

### 2. Add columns

Inside the list → **+ Add column** → choose type:

* **Text**
* **Number**
* **Date**
* **Choice**
* **Person**
* **Lookup**
* **Yes/No**

### 3. Create views

**List → Create view** → choose **Standard, Calendar, Datasheet, or Gallery** view → customise filters and sort.

### 4. Use the list as a data source

The list is now available to **Power Automate, Power Apps, and Highlighted Content** web parts.

---

## Task 7.2 — Display a Calendar

### 1. Add Events web part or Calendar web part

**Edit page → '+' → 'Events'** or search **'Group Calendar'** → select and configure.

### 2. Link to a SharePoint Events list

**Web part settings → Source → This site** → select the Events list created in Task 7.1.

### 3. Set Calendar view in the List

Go to the list → **+ Add view → Calendar** → map **Start Date** and **End Date** columns.

---

## Task 7.3 — Create a Form to Start a Process

### 1. Customise the list form

Open list → **+ New → Customise with Power Apps** → design the form fields and layout.

### 2. Add validation

In Power Apps form designer, add data validation rules and required field indicators.

### 3. Trigger Power Automate

In Power Automate: SharePoint **'When an item is created'** trigger → add approval/notification steps.

### 4. Embed form on a page

**Edit SP page → '+' → Microsoft Forms** OR add a **button Quick Link** pointing to the list's New Form URL.

---

## Task 7.4 — Use JSON to Format List Items

### 1. Open column formatting

Click the column header → **Column settings → Format this column**.

### 2. Enter JSON code

Paste or type JSON. Example: colour a **'Status'** choice column green/red based on value.

### 3. Apply view formatting

Alternatively, use **View formatting → Advanced mode** → paste row-level JSON for card or grouped views.

### 4. Save and preview

Click **Save** — the list immediately reflects the new visual format.

---

## 💡 Best Practice Tips

* 🧩 **Use ready-made JSON templates:** Use the SharePoint List Formatting GitHub repository (`pnp/List-Formatting`) for ready-made JSON templates.
* 📊 **Manage large lists carefully:** Keep lists under 5,000 items viewable — create indexed columns on frequently filtered fields to avoid list-view threshold errors.
* ⚡ **Use Datasheet view for bulk entry:** Use **'Datasheet view'** for bulk data entry instead of opening each item individually.
* 🎨 **Use Power Apps for enhanced forms:** Power Apps forms provide a far richer UX than the default SharePoint new/edit form.
