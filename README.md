# Invoice Automation using UiPath

This project automates the extraction of data from multiple invoice Excel files and consolidates it into a single summary report. It eliminates manual data entry by reading key fields (supplier, address, items, tax details, total amount, etc.) and generating a formatted summary sheet.

---

## Features
- Reads multiple invoice files from a folder.
- Extracts key fields like **Supplier, Address (with Pincode), Items, Invoice Date, Tax Percentage, Tax Amount, Total Amount**.
- Handles multiple items dynamically for each invoice.
- Consolidates all invoices into a **Daily Summary** Excel report.
- Automatically updates header with **latest invoice date**.
- Ensures consistent formatting (tables, auto formulas, date formatting).

---

## Tech Stack
- **UiPath Studio** (RPA)
- **Excel Automation Activities**
- **VB.NET / UiPath Expressions**

---

## Project Structure
Invoice-Automation-UiPath/

├── Main.xaml # Main workflow
|── input/ # Folder containing invoice files
|── output/ # Generated summary Excel
|── README.md # Documentation

---

## How It Works
1. Place invoice Excel files in the **input** folder.
2. Run the UiPath workflow.
3. The bot reads each invoice, extracts details from specific cells (B4, B5, B6, B20 onwards for items).
4. Merges all data into a **summary DataTable**.
5. Writes the summary into an Excel file (`Daily Summary.xlsx`) in the output folder.
6. Updates the title to include the latest invoice date.

---

## Usage
- Install dependencies: `UiPath.Excel.Activities`, `UiPath.System.Activities`.
- Update file paths in the workflow (input and output folders).
- Execute the `Main.xaml` in UiPath Studio or Orchestrator.
