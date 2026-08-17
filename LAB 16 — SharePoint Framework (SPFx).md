# LAB 16 — SharePoint Framework (SPFx)

## 🎯 Objective

Create custom web parts, extensions, and solutions using SPFx to extend SharePoint beyond out-of-the-box capabilities.

## 📋 Prerequisites

* Node.js 18.x
* Yeoman & Gulp
* VS Code
* SharePoint tenant with App Catalog
* SPFx 1.18+

---

## Task 16.1 — Set Up the SPFx Development Environment

### 1. Install Node.js

Download Node.js 18.x LTS from `nodejs.org`.

Verify the installation in the terminal:

```bash
node -v && npm -v
```

### 2. Install Yeoman & Gulp

```bash
npm install -g yo gulp @microsoft/generator-sharepoint
```

### 3. Scaffold a project

Create a folder → run:

```bash
yo @microsoft/sharepoint
```

Follow the prompts:

* Solution name
* Component type (**Web Part**)
* Framework (**React / No Framework**)

### 4. Trust the dev certificate

Run once to allow local HTTPS serving:

```bash
gulp trust-dev-cert
```

### 5. Run local workbench

Run:

```bash
gulp serve
```

The browser opens at:

```text
https://localhost:4321/temp/workbench.html
```

Use the local workbench to test the web part.

---

## Task 16.2 — Build and Deploy a Custom Web Part

### 1. Develop the web part

Edit:

```text
src/webparts/[yourWebPart]/[YourWebPart].ts
```

or, for React:

```text
src/webparts/[yourWebPart]/[YourWebPart].tsx
```

Add properties and render logic.

### 2. Build the solution

Run:

```bash
gulp build
```

This compiles TypeScript and SCSS.

### 3. Bundle & package

Run:

```bash
gulp bundle --ship && gulp package-solution --ship
```

This creates a `.sppkg` file in the:

```text
sharepoint/solution
```

folder.

### 4. Upload to App Catalog

**SharePoint Admin Center → Apps → App Catalog** → upload the `.sppkg` → check **'Make this solution available to all sites'**.

### 5. Add web part to a page

On any SharePoint page → **Edit → '+'** → find your custom web part → add and configure.

---

## 💡 Best Practice Tips

* 🚀 **Use production builds:** Always use `gulp bundle --ship` and `package-solution --ship` for production builds — debug builds are large and slow.
* 🧪 **Test in the hosted workbench:** Test in the hosted workbench (`your-tenant.sharepoint.com/_layouts/15/workbench.aspx`) before App Catalog deployment.
* 🔢 **Follow semantic versioning:** Use semantic versioning in `package-solution.json` — increment the version on every update.
* 🧩 **Use PnP JS:** Use PnP JS (`pnpjs.com`) inside SPFx for elegant SharePoint REST API calls without raw `fetch`.
* 🧑‍💻 **Use a dedicated development tenant:** Join the Microsoft 365 Developer Program (`developer.microsoft.com/en-us/microsoft-365/dev-program`) for a free dev tenant.
