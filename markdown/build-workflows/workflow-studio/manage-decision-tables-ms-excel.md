---
title: Manage decision tables in Excel
description: If you have large decision tables to build or want to enhance decision tables outside of the ServiceNow AI Platform, manage them in Excel. Export a decision table to an Excel file, edit the downloaded file to add and edit rows, and then import the file back into Workflow Studio.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Using decision tables, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Manage decision tables in Excel

If you have large decision tables to build or want to enhance decision tables outside of the ServiceNow AI Platform, manage them in Excel. Export a decision table to an Excel file, edit the downloaded file to add and edit rows, and then import the file back into Workflow Studio.

## Exporting a decision table to Excel

After creating and saving inputs, condition columns, and result columns, export a decision table to Excel in `.xlsx` format by selecting **Export**. The exported file contains two worksheets: One with the decision table and the other with instructions on how to build decision rows and prevent import errors.

Editing your decision tables in Excel can help you build large tables more quickly. It also gives you the ability to assign the structural setup to a developer, and then delegate rule authoring to someone else, who could fill it out in Excel.

**Note:** If you have any advanced rows in your decision table when you export to Excel, these rows are read-only and cannot be edited in Excel. You can edit the rest of the table in Excel and import it back into Workflow Studio.

## Modifying the decision table in Excel

After you export a decision table to Excel, you can add, remove, edit, or reorder decision rules. Follow these directions to build your decision table.

-   Build conditions using the operator and value columns.
    -   In each **Operator** cell, choose the relevant operator from the drop-down list. The operator list is specific to the condition column field type.
    -   In each **Value** cell, enter or select the condition value, following the format guidance from the instructions sheet.
    -   When building date, due date, date/time, reference, or choice conditions, you can select a value from the drop-down list.
-   Specify result values.
    -   In each **Result** cell, enter the result value.
    -   For reference or choice results, select a result value from the drop-down list.

Consider the following limitations when modifying a decision table in Excel.

-   Use Excel to add, remove, or edit decision rules, but do not use Excel to add or modify condition columns or result columns.
-   Edit only cells in the **Condition** and **Result** columns. During the import, any data entered to the right of these columns are ignored.
-   Retain the headers in the exported file, and do not modify them in any way.
-   Modify only the original exported file in Excel. Do not copy and paste the contents of an exported file into a new Excel file. However, the original file can be renamed.
-   Ensure that there are no empty rows. Any entry after five consecutive empty rows is ignored.

## Importing an Excel file into Workflow Studio

**Note:** The import option is only available after you export the decision table to Excel.

During the import process, all the modifications in the Excel file are validated before your changes are imported to Workflow Studio. The following outcomes are possible while attempting to import.

-   **Successful import**: The Excel file import is successful. The Import window closes automatically, and your decision table is updated with the imported data. Save your changes before continuing.
-   **Failed import**: The Excel file import has failed. Download the `Error.xlsx` file that contains the detailed description about the errors and how to fix them. After fixing the errors, follow the import process and import the corrected error file.

## View export and import history

View the export and import history of a decision table in the History sidebar. Each entry displays the name of the user who imported or exported the file and the timestamp.

You can download the relevant Excel file based on the history type: The exported file \(Export Successful\), the imported file \(Import Successful\), or the error file \(Import Failed\). History records are not created when you select **Cancel** in the import window.

**Note:** The `glide.ui.export.choice_list_max_characters` property sets the maximum number of characters that will be included from a condition field type when exporting to Microsoft Excel, as well as the maximum number of characters displayed in the list view condition builder in Core UI. This property is of type integer and has a default value of 80. To use this property, add it to the System Property \[sys\_properties\] table. It's important to note that this property does not affect the length of condition field values in tables.

## Limitations

The following are scenarios when you cannot modify a decision table in Excel.

-   Decision table does not contain a conditions column.
-   Decision table has unsaved changes.
-   Decision table has condition columns with unsupported field types.
-   Decision table has a condition column that is related to an inactive input.

**Note:** The Localization Framework is integrated in decision tables. However, because the Edit in Excel feature doesn’t support localization, you cannot use this feature in any instance that doesn't use English.

**Parent Topic:**[Using decision tables](using-decision-builder.md)

