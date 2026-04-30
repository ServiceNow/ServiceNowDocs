---
title: Add a record in the template
description: Add rows to the template to create new records.
locale: en-US
release: zurich
product: Easy Import
classification: easy-import
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Easy import, Imports, Workflow Data Fabric]
---

# Add a record in the template

Add rows to the template to create new records.

## Before you begin

Role required: admin.

**Note:** The template only imports records on the first page of the template. The import process ignores all other pages.

## About this task

![](../image/EasyImportInsertTemplate.png "Easy import insert template")

## Procedure

1.  Add a row for each record you want to add to the table.

    Each column corresponds to a field in the target table. Use the UI [Field administration](https://www.servicenow.com/docs/access?context=c_IntroductionToFields&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) to learn about the purpose and content of the field.

    The template validates values as you enter them and highlights cells containing invalid data. While you do not have a provide a value for every column, certain fields may fail validation if you do not provide a value.

2.  Review any highlighted cell and resolve the issue.

3.  When you finish entering new rows, save the spreadsheet as an Excel Workbook.

    The insert templates uses special processing for certain fields:

    -   Created by Field: The insert template always lists the system administrator user \(admin role\) in the Created by field regardless of whether the import includes a Created by column. Even if you provide a different user value in the template, the import process overwrites this value with the system administrator user.
    -   Blank Values: Leaving a cell blank in the insert template results in a blank value in the imported record, provided the field supports a blank value. Fields that do not support a blank value will produce a validation error if you provide a blank value.

**Parent Topic:**[Easy import](../concept/c_EasyImport.md)

