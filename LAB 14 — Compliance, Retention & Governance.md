# LAB 14 — Compliance, Retention & Governance

## 🎯 Objective

Apply retention labels, manage controlled documents with versioning and approvals, and geolocate sites to data centres.

## 📋 Prerequisites

* Microsoft Purview (Compliance) access
* SharePoint Admin
* Global Admin for geo configuration

---

## Task 14.1 — Apply Labels for Content Retention Policies

### 1. Create a Retention Label

**Microsoft Purview portal (`compliance.microsoft.com`) → Data lifecycle → Retention labels → + Create a label**.

### 2. Configure retention settings

Set:

* **Retain items for X years**
* **Delete after period**
* **Based on when created or labelled**

### 3. Publish the label

Create a **Label policy → Publish to** → select SharePoint sites → **Save**.

### 4. Apply in SharePoint

In a **Document Library → Library Settings → Apply label** → choose the published label, OR users can apply manually per file.

### 5. Verify

Select a file → **Details pane** → check the **Retention label** field shows the applied label.

---

## Task 14.2 — Manage Controlled Documents with Versioning & Approvals

### 1. Enable Versioning

**Library Settings → Versioning settings** → **Create major and minor (draft) versions** → **Require content approval: Yes**.

### 2. Configure approvers

Set **'Who should see draft items'** → **Only users who can approve items**.

### 3. Submit for approval

Edit and save a document → it becomes a draft (**0.1**) → submit for approval.

### 4. Approve or reject

Approver: open file → **'...' → Approve/Reject** → add comments → submit.

### 5. Published version

On approval, the minor version promotes to the next major version visible to all readers.

---

## Task 14.3 — Geolocate Sites to Different Data Centres

### 1. Prerequisite: Multi-Geo licence

Microsoft 365 Multi-Geo is an add-on licence. Confirm with your Microsoft account team.

### 2. Configure a Satellite geo location

**SharePoint Admin Center → Sites → Geo locations → Add satellite location** → choose region (e.g., **EUR, APC**).

### 3. Create a site in the geo

When creating a new site, set the **'Preferred data location'** to the satellite geo.

### 4. Verify geo

**Site → Site Settings → Site Information → Geo location** field confirms the data residency.

---

## 💡 Best Practice Tips

* 🧪 **Test retention labels first:** Test retention labels in a sandbox tenant before applying to production — accidental deletion locks are hard to reverse.
* 🔒 **Control document editing:** Enable **'Require Check Out'** on strictly controlled document libraries to prevent simultaneous edits.
* 📦 **Set a version limit:** Set a version limit (e.g., **50 major versions**) to prevent storage bloat.
* 🌍 **Plan Multi-Geo carefully:** Multi-Geo is primarily for data residency compliance (GDPR) — plan your geo map before provisioning.
