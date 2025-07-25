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

### Main workflow
├── Main.xaml 
### Folder containing invoice files (user created)
|── input/ 
### Generated summary Excel (user created)
|── output/ 
### Documentation 
|── README.md 

---

> **Note**: `input` and `output` folders are not included in this repo. You must create them manually after cloning the project.

---

## How It Works
1. Create two folders in your local project directory:
   - `input` → place invoice Excel files here.
   - `output` → this will hold the generated summary file.
2. Open `Main.xaml` in UiPath Studio.
3. Install required dependencies from `project.json` (UiPath will prompt you).
4. Run the workflow:
   - It reads invoice files from `input/`.
   - Extracts details from defined cell locations.
   - Writes summarized data to `output/Daily Summary.xlsx`.

---

## Required Dependencies
- UiPath.Excel.Activities
- UiPath.System.Activities

These are defined in `project.json`. UiPath Studio will auto-restore them on open.

---

## Usage
- Clone the repository:
```bash
git clone <repo-url>
```bash
- Create input and output folders inside the project folder.
- Place your invoice files in input and run the workflow in UiPath Studio.

---

## Usage
- Install dependencies: `UiPath.Excel.Activities`, `UiPath.System.Activities`.
- Update file paths in the workflow (input and output folders).
- Execute the `Main.xaml` in UiPath Studio or Orchestrator.
