# LAB 18 — Recycle Bin & Site Recovery

## 🎯 Objective

Restore accidentally deleted items from the SharePoint Site Recycle Bin and understand the two-stage Recycle Bin process.

## 📋 Prerequisites

* SharePoint site
* Appropriate permissions:

  * **Members** can restore own items
  * **Owners** see all
  * **Admin** sees Site Collection Recycle Bin

---

## Task 18.1 — Restore Items from the Site Recycle Bin

### 1. Open the Recycle Bin

On the site home page → left navigation → **Recycle Bin** (or **Site Contents → Recycle Bin** button at top).

### 2. Find the deleted item

Browse or use the search/filter at the top.

Recycle Bin shows:

* **Name**
* **Location**
* **Deleted by**
* **Deleted date**

### 3. Restore a single item

Tick the checkbox next to the item → **Restore** (appears at top).

The item returns to its original location.

### 4. Restore multiple items

Tick multiple checkboxes → **Restore** → all selected items are restored.

### 5. Permanently delete

If you want to free space, select item → **Delete (from Recycle Bin)** → moves to **Second-Stage**.

---

## Task 18.2 — Second-Stage Recycle Bin (Site Collection Level)

### 1. Access as Site Collection Admin

**Site Settings → Site Collection Administration → Recycle Bin** → select **'Deleted from end user Recycle Bin'**.

### 2. Restore from second stage

Select the item → **Restore** → it returns to the first-stage Recycle Bin and then to the original location.

### 3. Understand retention

Items stay in the first-stage Recycle Bin for **93 days**. After that (or after manual deletion), they move to the second-stage for another **93 days**.

### 4. Admin-level recovery

If both stages are exhausted, raise a support ticket with Microsoft — restoration is not guaranteed after **93+93 days**.

---

## 💡 Best Practice Tips

* ♻️ **Educate users about the Recycle Bin:** Many users raise urgent tickets for items they can restore themselves in seconds.
* 🔍 **Review the Recycle Bin regularly:** Site owners should check the Recycle Bin weekly for large items accidentally deleted.
* 🗂️ **Use versioning as an additional safety net:** For critical files, enable versioning — even overwritten content can be recovered.
* ⚖️ **Use eDiscovery holds when required:** Use the **'eDiscovery'** hold in Microsoft Purview if legal preservation requires preventing permanent deletion.
* 🛡️ **Track deletion events:** Use the **Microsoft Purview Audit log (`compliance.microsoft.com`)** to track deletion events for security reviews.
