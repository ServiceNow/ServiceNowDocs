---
title: Matrix Loader
description: Learn how the Matrix Loader accelerates configuration management by simplifying large-scale data creation, updates, and migrations across your ServiceNow CPQ environments.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-09-17"
reading_time_minutes: 4
breadcrumb: [ServiceNow CPQ Configurator, ServiceNow CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Matrix Loader

Learn how the Matrix Loader accelerates configuration management by simplifying large-scale data creation, updates, and migrations across your ServiceNow CPQ environments.

The Matrix Loader is a bulk data management utility that enables administrators to efficiently add, edit, and migrate configuration elements such as fields, field options, rules, layouts, product pickers, and tables. Instead of creating elements one by one in the Admin interface, the Matrix Loader lets you define configurations in CSV files—making it ideal for scaling complex implementations, backing up configurations, and moving data between test and production environments.

The Matrix Loader ensures data integrity and consistency by automatically validating dependencies \(for example, between fields and field options\) and uploading elements in the correct order. Administrators can also use the Matrix Loader to export CSV templates and sample files, providing a quick reference for valid column structures, accepted values, and upload formats.

## Key concepts

-   CSV structure: Each configuration type has a specific column schema. Administrators can rearrange columns as long as headers remain correct.
-   Import order: The loader auto-sorts uploads logically \(for example, fields → field options → rules\).
-   Validation and error handling: Errors during upload usually result from missing required columns, invalid references, or mismatched names. The Matrix Loader displays error messages to help correct them quickly.
-   Export and backup: All configuration entities can be exported from the Admin interface to create reusable CSV backups.
-   No redeployment for tables: Updates to managed tables take effect immediately. However, rules referencing those tables require redeployment if modified.

## Key benefits

The Matrix Loader eliminates the repetitive and time-consuming steps involved in large-scale setup or updates. It provides several key advantages:

|Benefit|Description|
|-------|-----------|
|Efficiency|Upload hundreds of fields, rules, or tables in one batch instead of creating them manually.|
|Consistency|Maintain consistent configurations across environments with reusable CSV definitions.|
|Traceability|Use exported CSV files as a versioned record of environment data for audits or rollback.|
|Migration support|Seamlessly migrate configurations from sandbox to production environments.|
|Error handling|Validate and confirm successful uploads before committing changes.|
|No-code automation|Modify configurations and relationships without scripting.|

## Matrix Loader configuration types

The Matrix Loader supports multiple configuration types, each designed to streamline a specific aspect of the ServiceNow CPQ setup:

|Upload Type|Purpose|Example Use Case|
|-----------|-------|----------------|
|Fields and field options|Create and manage fields, picklists, and product pickers.|Add 200 product options to a field at once.|
|Rules|Define business logic, calculations, and conditional visibility.|Upload all visibility and determination rules for a blueprint.|
|Layouts|Design user experiences by defining field placement and grouping.|Update layout structure across multiple blueprints.|
|Tables|Manage data sets used for lookups and dynamic logic.|Import pricing data or reference mappings.|
|Product pickers|Define product selection fields and their behaviors.|Bulk upload accessory or component data.|

## How the Matrix Loader works

The Matrix Loader performs uploads in a controlled sequence to maintain relational accuracy between configuration elements. Here’s how the process works:

1.  Prepare data files: Define configuration elements in spreadsheet tools such as Google Sheets or Microsoft Excel, and export each sheet as a CSV file.
2.  Access the Matrix Loader: in the left Admin navigation pane, click **Matrix Loader**.
3.  Export sample templates \(optional\): Download sample CSVs for fields, field options, rules, or tables to use as reference templates.
4.  Upload files: Drag and drop one or more CSV files. The Matrix Loader automatically detects file types based on filename keywords.
5.  Validate mappings: Confirm that the Matrix Loader correctly identified each upload type \(for example, fields vs. rules\).
6.  Import and verify: Click **Import**. The Matrix Loader runs each upload in the correct sequence. Review success or error notifications in the Notification Center.
7.  Confirm configuration: Verify new and updated items on the relevant Admin pages \(such as fields or rules\).

**Note:** The Matrix Loader automatically performs dependency resolution—for example, ensuring that fields upload before field options or that rule dependencies are validated.

## Example use cases

-   Bulk onboarding: Create hundreds of picklists, rules, and layout mappings for a new product line in minutes.
-   Environment migration: Move configuration data from sandbox to production using standardized CSV exports.
-   Mass update: Change field types, rule actions, or default values across multiple blueprints simultaneously.
-   Backup and restore: Export CSVs regularly to maintain a recoverable version of your configuration.

**Related topics**  


[Configure the Matrix Loader](cpq-using-the-matrix-loader.md)

[Matrix Loader CSV fields and field options upload and export](cpq-matrix-loader-csv-fields-and-field-options-upload-and-export.md)

[Matrix Loader: CSV rules upload](matrix_loader_csv_rules_upload.md)

[Matrix Loader: CSV table upload](../task/cpq-matrix-loader-csv-table-upload.md)

