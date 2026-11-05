# Task 1: Data Cleaning and Preprocessing — Sales Data

## Project overview
This beginner-level project demonstrates how to inspect and clean a small sales dataset using spreadsheet concepts. The workbook contains the original data, cleaned data, and a summary of changes.

**Dataset note:** The included sales records are an illustrative practice dataset created for this project. They are not real customer or company records and are not represented as a Kaggle or employer-provided dataset. If your mentor has provided a specific dataset, use that dataset instead.

## Files
- `raw_sales_data.csv` — original practice data with deliberately introduced data-quality issues.
- `cleaned_sales_data.csv` — cleaned output.
- `Task_1_Sales_Data_Cleaning.xlsx` — Excel workbook with `Raw_Data`, `Cleaned_Data`, `Cleaning_Summary`, and `Read_Me_First` sheets.

## Cleaning steps demonstrated
1. Checked for missing and invalid values.
2. Removed duplicate records and retained the first record for each Order ID.
3. Trimmed extra spaces and standardized text capitalization.
4. Converted order dates to `DD-MM-YYYY`; unrecognized dates were left blank rather than guessed.
5. Converted Quantity and Unit Price to numeric values.
6. Replaced missing/invalid Quantity with the median quantity (1.5, rounded to 2 because Quantity is a whole-number field).
7. Replaced missing Region with `Unknown`.
8. Added `sales_amount`, calculated as `quantity × unit_price`.
9. Renamed headers to lowercase with underscores.

## How to review in Excel
1. Open `Task_1_Sales_Data_Cleaning.xlsx`.
2. Start with `Read_Me_First`.
3. Compare `Raw_Data` with `Cleaned_Data`.
4. Check the actions and counts in `Cleaning_Summary`.
5. If you need to reproduce the work manually, use Excel's **Remove Duplicates**, **Filter**, **Find & Replace**, **Text to Columns** or date formatting, and formulas such as `=G2*H2` for Sales Amount.

## Important note about decisions
- Median imputation is used only for missing/invalid Quantity in this demonstration.
- A missing Region is labelled `Unknown`.
- An invalid date is left blank because the correct date cannot be inferred safely.
- The first record is retained when Order ID is duplicated.

## Before submitting
Review the workbook and make sure you can explain each cleaning decision. If your internship instructions require a real dataset from Kaggle or a mentor-provided source, replace the illustrative data with that source and repeat the cleaning process. Do not describe this practice dataset as real company data.
