---
title: Run transform to import spend category data into the Spend Category primary table
description: Run transform to import the data records from the Spend Category Stage \(sn\_spend\_mgmt\_category\_stage\) staging table into the Spend Category \(sn\_spend\_mgmt\_category\) primary table.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [run transform, import spend category data, import data into Spend Category table, spend category table, import data records into the Spend Category table]
breadcrumb: [Map spend categories to product categories, Using Spend and Savings Management, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Run transform to import spend category data into the Spend Category primary table

Run transform to import the data records from the Spend Category Stage \(sn\_spend\_mgmt\_category\_stage\) staging table into the Spend Category \(sn\_spend\_mgmt\_category\) primary table.

## Before you begin

Role required: admin

## About this task

Here’s how the transform map works:

-   In the Spend Category table, only the Category name field is mandatory and must be unique. All other fields are optional.
-   During transformation, if either the Spend category manager or Sourcing manager isn’t found, the Spend category record is skipped and an error is logged.
-   If the Parent spend category doesn’t exist, it’s created automatically.
-   If a matching Product category can’t be found using either the UNSPSC or Category name, the corresponding many-to-many \(m2m\) record isn’t created, and the issue is logged accordingly.

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Load Data**.

2.  Select **Existing table**.

3.  In the **Import set table** field, select **Spend Category Stage \(sn\_spend\_mgmt\_category\_stage\)**.![Displays the Load Data window in which you can import a set table and select the source for the import.](../image/import_spend_category.png)

4.  In the **Source of the import** field, select **File**.

5.  Select **Choose File** and select the source Excel spreadsheet.

6.  Specify the worksheet number in the **Sheet number** field and header row number in the **Header row** field.

7.  Select **Submit**.

    The imported data is now available in the new Import Set table.

8.  Select **Run Transform**.

    **Important:** Ensure that the **Import set** field shows sn\_spend\_mgmt\_category\_stage and the **Selected maps, run in order** field shows Load spend categories and map to product categories - sn\_spend\_mgmt\_category.

9.  Select **Transform**.

    The data records are imported into the Spend Category \(sn\_spend\_mgmt\_category\) primary table.

10. Verify that the data records were imported into the Spend Category \(sn\_spend\_mgmt\_category\) primary table.


