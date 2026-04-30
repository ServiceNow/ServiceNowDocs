---
title: Download an import template
description: Select the list you want to import data to and create an import template from that list.
locale: en-US
release: xanadu
product: Easy Import
classification: easy-import
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Easy import, Imports, Creating integrations with applications]
---

# Download an import template

Select the list you want to import data to and create an import template from that list.

## Before you begin

Role required: admin.

## Procedure

1.  Navigate to any list, such as **All** &gt; **Self-Service** &gt; **Incidents**.

2.  Right-click the column heading.

3.  Select **Import**.

    **Note:** Make sure columns are updated before importing them.

4.  Select if you want to **Insert** or **Update** records.

    |Template|Description|
    |--------|-----------|
    |Insert|Use this template to add new records to a table.|
    |Update|Use this template to change values within existing records in a table. This template contains one row for each record in the list. The current list filter determines what records the template contains.|

5.  Clear the **Include all fields in the template?** check box to include only columns that appear in the list in the template.

    Certain fields in the table are updated by system processes, and you cannot import values into them. An example is the **Created by** field, which is populated during import with the logged-in user who performs the import.

    Leave this check box selected to include all columns from the table in the template, even those columns that are hidden in the list.

6.  Select the **Export template format** you want, either **XLS** or **XLSX**.

    XLSX is the preferred format, XLS is available for legacy support. The **Export template format** field appears only if the property **glide.legacy.excel.export** is true.

7.  Click **Create Excel template**.


## What to do next

Open the spreadsheet using your preferred application.

**Note:** Each template contains a Directions tab describing how to use the template.

**Parent Topic:**[Easy import](../concept/c_EasyImport.md)

