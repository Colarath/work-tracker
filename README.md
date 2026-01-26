# Cloud Work Tracker 🕒

A serverless, mobile-friendly web application to track daily work hours, calculate overtime variance, and sync data across devices using the cloud. 

Built with **HTML, Bootstrap 5, and JavaScript**. No Python backend or complex server required.

## 🚀 Features

* **Global Running Balance:** Instantly see if you are in credit (Green) or debit (Red) based on a standard 8-hour work day.
* **Cloud Sync:** Uses [JSONBin.io](https://jsonbin.io) to store your history. Log hours on your phone, view them on your PC.
* **Manual Sync Control:** "Load" and "Save" buttons allow you to control when you update the cloud, preserving API request limits.
* **CSV Export:** Download your entire work history to Excel/Numbers with one click.
* **Mobile Optimized:** Designed to look like a native app when added to your phone's Home Screen.
* **Privacy Focused:** API keys are stored in your browser's Local Storage, not in the code.

## 🛠️ Setup Guide

To use this app, you need a free cloud storage bin.

### 1. Get your API Keys
1.  Go to [JSONBin.io](https://jsonbin.io) and sign up/login.
2.  Click **Create Bin**.
3.  Paste an empty list `[]` into the editor and click **Create**.
4.  Copy the **Bin ID** (e.g., `653ad...`).
5.  Go to the **API Keys** section and copy your **X-Master-Key** (e.g., `$2a$10...`).

### 2. Installation
You have two options:

**Option A: Run Locally**
* Download `index.html`.
* Double-click it to open in any web browser.

**Option B: Host for Free (Recommended)**
* Upload `index.html` to a GitHub Repository.
* Go to **Settings > Pages**.
* Select `main` branch and click Save.
* Your app will be live at `https://yourusername.github.io/repo-name/`.

### 3. First Run Configuration
1.  Open the app.
2.  A **Settings** modal will appear automatically.
3.  Paste your **Bin ID** and **X-Master-Key**.
4.  Click **Save**.
5.  *Note: These keys are saved in your browser, so you don't need to enter them again unless you clear your cache.*

## 📱 How to Use

### Logging Time
1.  Select the **Date** (defaults to Today).
2.  Enter **Hours Worked** (e.g., `8.5`).
3.  Click **Add**.
4.  *Note: This saves the entry to your device immediately, but not the cloud.*

### Syncing
* **Save (Upload):** When you are finished logging, click the **Save** button to push your changes to the cloud. An indicator dot will show if you have unsaved changes.
* **Load (Download):** If you switch devices (e.g., from phone to PC), click **Load** to fetch the latest data.

### Analysis
* **Filter:** Use the dropdown menu to view history for a specific month.
* **Export:** Click **Export CSV** to download a spreadsheet compatible with Excel.

## ⚙️ Technical Details
* **Frontend:** HTML5, CSS3 (Bootstrap 5.3).
* **Logic:** Vanilla JavaScript (ES6+).
* **Storage:** JSONBin.io (via REST API).
* **Standard Hours:** Hardcoded to 8 hours (Change `const STANDARD_HOURS = 8;` in the source code to adjust).

---
*Created for personal productivity.*
