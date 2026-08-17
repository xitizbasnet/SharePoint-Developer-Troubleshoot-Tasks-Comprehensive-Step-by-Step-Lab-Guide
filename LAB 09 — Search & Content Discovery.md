# LAB 09 — Search & Content Discovery

## 🎯 Objective

Customise SharePoint search result pages, create custom result templates, and deploy PnP Modern Search web parts.

## 📋 Prerequisites

* SharePoint site
* Site Collection Admin
* PnP Modern Search solution deployed (for Task 9.3)

---

## Task 9.1 — Search for Content in SharePoint

### 1. Use the search bar

Click the search box at the top of any SharePoint page → type your keyword.

### 2. Filter results

On the search results page, use filters (**File type, Modified date, Author**) on the left panel.

### 3. Search within a site

On a site, press **Enter** after typing to scope results to that site only.

### 4. Use KQL for precise queries

In the search box use KQL:

```text
FileType:pdf Author:"John Smith"
```

or:

```text
contenttype:"Project Proposal"
```

---

## Task 9.2 — Create Custom Search Result Templates

### 1. Open Search Settings

**Site Collection Settings → Search → Search Result Types → New Result Type**.

### 2. Define conditions

Set **What content should match this rule** → choose content source and property conditions.

### 3. Create a display template

Map managed properties and design an HTML snippet for how results are displayed.

### 4. Test

Search for a known item and confirm the custom result template renders correctly.

---

## Task 9.3 — Custom Search Pages with PnP Modern Search

### 1. Download PnP Modern Search

Get the latest release from `github.com/microsoft-search/pnp-modern-search/releases`.

### 2. Deploy the solution

Upload the `.sppkg` file to the **App Catalog** → **Trust** → **Deploy**.

### 3. Add to your site

**Site Contents → + New → App → PnP Modern Search** → add to site.

### 4. Build search page

Edit a page → add **'Search Results'**, **'Search Box'**, and **'Search Filters'** web parts → configure properties.

### 5. Customise layout

In the **Search Results** web part → **Layout** → choose **Cards, List, Debug, or Custom Adaptive Card**.

---

## 💡 Best Practice Tips

* 🔖 **Promote frequently needed content:** Use **'Bookmarks'** in Microsoft Search (**admin.microsoft.com → Search → Answers → Bookmarks**).
* 🔍 **Monitor crawl and search configuration:** Crawl errors affect search — monitor the search schema and managed properties in SharePoint Admin Center.
* 🧩 **Reuse PnP Modern Search templates:** PnP Modern Search allows templating via **Handlebars** — reuse community templates from the PnP repo.
* ⚡ **Use lightweight alternatives when appropriate:** Use **'Content Search'** and **'Highlighted Content'** web parts as lightweight alternatives to PnP for simple scenarios.
