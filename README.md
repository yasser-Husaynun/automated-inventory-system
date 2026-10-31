# 📦 Automated Inventory Notification System

An automated backend workflow designed to monitor product inventory levels in real-time and dispatch instant email alerts when stock thresholds are breached. Built using **Make.com**, **Google Sheets**, and **Gmail API**.

---

## 🛠️ Tech Stack & Tools

* **Workflow Automation:** Make.com
* **Database / Data Source:** Google Sheets
* **Notification Service:** Gmail API
* **Logic & Filtering:** Conditional Array Filtering (`Current Stock <= Reorder Level`)

---

## ⚙️ How It Works

1. **Data Ingestion:** The scenario queries the Google Sheets inventory database to fetch row data (Product Name, Current Stock, Reorder Level).
2. **Conditional Filtering:** A logic filter checks each record to see if `Current Stock` is less than or equal to `Reorder Level`.
3. **Alert Dispatch:** For qualifying rows, an automated HTML/Text email alert is triggered via the Gmail API to notify the inventory management team.

---

## 📊 System Architecture

`[Google Sheets: Search Rows]` ➡️ `[Filter: Stock <= Reorder]` ➡️ `[Gmail: Send Email]`

---

## 🚀 Setup & Installation

1. Clone this repository or download the `blueprint.json` file.
2. Open your [Make.com](https://www.make.com) dashboard.
3. Create a new scenario and select **Import Blueprint** from the bottom control bar.
4. Upload `blueprint.json` and map your Google Sheets & Gmail OAuth credentials.
