# Procedure Builder Prototype

This project is a single-page web application that provides a wizard-style interface for defining a business procedure, its associated data tables (inputs and outputs), and exporting the entire definition as a structured JSON or YAML file.

## Features

* **Multi-Step Wizard:** Guides the user through the process of defining a procedure.
* **Procedure Definition:** Capture the name and a summary of the business procedure.
* **Input & Output Tables:** Define the tables that the procedure reads from (inputs) and writes to (outputs).
* **Column Definition:** For each table, specify columns with a name and data type (e.g., `string(50)`, `int`, `float`).
* **Dynamic Table and Column Management:** Easily add or remove tables and columns from the definition.
* **Interactive Data Editor:**
  * A modal window to define or edit sample data for each table.
  * Features two synchronized views: an editable HTML grid and a CSV text area.
  * Changes in one view are instantly reflected in the other.
* **Review and Export:**
  * A final step to review the complete procedure definition.
  * Displays the output in both JSON and YAML formats.
  * Allows downloading the definition as a `.json` or `.yaml` file.

## How to Use

1. **Open the File:** Simply open the `index.html` file in any modern web browser. No web server or build process is required.
2. **Step 1: Procedure Details:** Enter a name and a summary for your procedure.
3. **Step 2: Input Tables:**
   * Click "+ Add Input Table" to create a new table definition.
   * Name the table and add its columns.
   * Optionally, click "Define/Edit Data" to open the data editor and provide sample data.
4. **Step 3: Output Tables:** Repeat the process for the tables the procedure will generate.
5. **Step 4: Review and Export:**
   * After clicking "Finish & Review", you will see the complete procedure definition.
   * You can review the generated JSON and YAML.
   * Click "Download JSON" or "Download YAML" to save the definition to your computer.

## Technical Details

* **Frontend:** The application is built with plain HTML, CSS, and modern JavaScript (ES6+).
* **No Dependencies:** It runs entirely in the browser and has no build dependencies. The only external library is `js-yaml`, which is loaded from a CDN to handle YAML generation.
* **State Management:** The application state is managed in a simple JavaScript object within a self-invoking function to avoid polluting the global scope.
