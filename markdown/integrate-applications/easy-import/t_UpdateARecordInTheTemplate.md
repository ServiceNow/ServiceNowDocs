---
title: Update a record in the template
description: Modify rows in the template to update existing records.
locale: en-US
release: yokohama
product: Easy Import
classification: easy-import
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Easy import, Imports, Data and Automation]
---

# Update a record in the template

Modify rows in the template to update existing records.

## Before you begin

Role required: admin.

**Note:** The template only imports records on the first page of the template. The import process ignores all other pages.

## About this task

![](../image/EasyImportUpdateTemplate.png "Easy import update template")

## Procedure

1.  Edit the row for each existing record to be updated and replace existing values with new values.

    Use the UI field hints to learn about the purpose and content of the field.

    The template validates values as you enter them and highlights cells containing invalid data. While you do not have a provide a value for every column, certain fields may fail validation if you do not provide a value.

2.  Review any highlighted cell and resolve the issue.

3.  When you finish updating existing rows, save the spreadsheet as an Excel Workbook \(.xls\).

    The insert templates uses special processing for certain fields:

    -   Updated by Field: The update template always lists the system administrator user \(admin role\) in the Updated by field regardless of whether the import includes an Updated by column. Even if you provide a different user value in the template, the import process overwrites this value with the system administrator user.
    -   Blank Values: The update template uses these rules when handling blank values in spreadsheet cells.
    |Original Value|New Value|Result|
    |--------------|---------|------|
    |Blank value|Any non-blank value|Valid update: the update changes the blank value to the new value.|
    |Any non-blank value|Blank value|Invalid update: the update preserves the existing non-blank value.|


**Parent Topic:**[Easy import](../concept/c_EasyImport.md)

