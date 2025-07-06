# Care4Sign - Advanced Report Analyzer

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Status: Active](https://img.shields.io/badge/status-active-success.svg)

A powerful, single-file, browser-based tool for analyzing and reconciling Care4Sign partner reports. This application allows you to upload your Excel reports directly in your browser, perform complex analysis without your data ever leaving your computer, and export the results.

It is designed to solve specific challenges like calculating merged commissions, identifying price discrepancies against a standard rate card, and comparing data against a second source.

---

## ✨ Key Features

*   **📊 BP Code Filtering:** Isolate and analyze data for a single Business Partner or view the entire report.
*   **➕ Merged Commission Calculation:** Select multiple commission columns (e.g., `Platin...`, `BP Co...`, `BP wis...`) and the tool will automatically sum them into a "Total Commission" for each transaction.
*   **💰 Price Variance Analysis:** Automatically compares the `Basic Price` in your report against a built-in standard rate card for different products and durations, instantly highlighting overcharges.
*   **⚖️ Source vs. Source Comparison:** Optionally upload a second report (e.g., a bank statement or payment gateway report) to find missing records or mismatched final prices.
*   **🔒 Secure & Private:** All file processing and analysis happens **100% in your browser**. Your data is never uploaded to a server.
*   **⬇️ Export to Excel:** Download a detailed report of the analysis, with each issue type separated into its own sheet for easy filtering and follow-up.

---

## 📸 Screenshot

*(It is highly recommended to add a screenshot of the application here to give users a visual preview.)*

 
*A preview of the application interface showing the upload, mapping, and results sections.*

---

## 🚀 How to Use

This is a standalone HTML file. No installation is required.

1.  **Download:** Download the `index.html` file from this repository.
2.  **Open:** Open the `index.html` file in a modern web browser like Chrome, Firefox, or Edge.
3.  **Load Files:**
    *   Click "Choose Files" under **Source 1** and select your main Care4Sign report(s). You can select multiple files; they will be merged automatically.
    *   (Optional) Upload a comparison file under **Source 2**.
4.  **Map Columns:** The tool will try to auto-detect columns. Verify that the correct columns from your report are selected in the **Column Mappings** section. Pay special attention to the multi-select `Commission Columns` field.
5.  **Set Options:** Use the **Analysis Options** to filter by a specific `BP Code` if needed.
6.  **Analyze:** Click the **Analyze Data** button.
7.  **Review & Export:**
    *   Review the high-level stats and summary cards.
    *   Switch to the "Detailed Report" tab to see all records for each issue.
    *   Click **Export Detailed Report** to save the findings as an `.xlsx` file.

---

##  mapping-guide Column Mapping Guide

For the analysis to work correctly, you must map these fields:

| Field Name           | Required | Description                                                                                             | Example Column(s) in Report        |
| -------------------- | :------: | ------------------------------------------------------------------------------------------------------- | ---------------------------------- |
| **Application ID**   |   Yes    | The unique identifier for each transaction.                                                             | `Applicati...`                     |
| **BP Code**          |   Yes    | The code for the Business Partner. Used for filtering.                                                  | `BP code`                          |
| **Product Name**     |   Yes    | The full product description, including duration (e.g., "CLASS 3 SIGNING 2 YEAR").                      | `Product...`                       |
| **Basic Price**      |   Yes    | The base price of the product, used for rate card comparison.                                           | `Basic ...`                        |
| **Final Price**      |   Yes    | The final amount charged to the customer.                                                               | `Price i...`                       |
| **Commission Columns** |    No    | **(Multi-select)** Choose all columns that constitute the partner's commission. They will be summed.    | `Platin...`, `BP Co...`, `BP wis...` |
| **Date**             |    No    | The date of the transaction.                                                                            | `Added Ti...`                      |

---

## 🛠️ Contributing

Contributions are welcome! If you have an idea for a new feature or have found a bug, please feel free to open a new issue.

1.  Fork the repository.
2.  Create a new branch (`git checkout -b feature/AmazingFeature`).
3.  Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4.  Push to the branch (`git push origin feature/AmazingFeature`).
5.  Open a Pull Request.

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
