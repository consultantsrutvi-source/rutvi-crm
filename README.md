# Rutvi Consultants – Internal CRM Tool

This is the internal CRM system used by **Rutvi Consultants** for managing:
- College Requirements
- Lecturer Data Collection
- Placement Tracking
- Bill Generation & EMI Scheduling
- Automated Google Sheet storage

This CRM is fully client-side (HTML + JS) and communicates with Google Sheets through
a published Google Apps Script Web App (`/exec` endpoint).

---

## 🔧 Setup Instructions

### 1. GitHub Pages Deployment
This repo is deployed using **GitHub Pages**.

**Steps**
1. Go to Settings → Pages
2. Choose:  
   **Source:** Deploy from branch  
   **Branch:** `main`  
   **Folder:** `/ (root)`
3. Save settings  
4. Your CRM will be available at:  
   `https://<username>.github.io/<repo>/`

---

## 📄 Google Apps Script Setup

### 1. Open Google Apps Script
Paste the full Apps Script code into Code.gs.

### 2. Update these fields:
- `SHEET_ID = "YOUR_SPREADSHEET_ID_HERE";`

### 3. Deploy Web App
Deploy → New Deployment → Web App:

- Execute as: **Me**
- Who has access: **Anyone**

Copy the `/exec` URL.

### 4. Replace SCRIPT_URL in index.html
In the HTML file:

```js
const SCRIPT_URL = "<YOUR_EXEC_URL>";
