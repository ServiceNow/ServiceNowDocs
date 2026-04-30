---
title: Load and map spend categories to existing product categories
description: As a Spend category admin, you can use spend category management to import your organization's spend categories and map them to ServiceNow product categories.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [load and map spend categories, map spend categories, map spend categories to product categories]
breadcrumb: [Map spend categories to product categories, Using Spend and Savings Management, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Load and map spend categories to existing product categories

As a Spend category admin, you can use spend category management to import your organization's spend categories and map them to ServiceNow product categories.

## Before you begin

Role required: sn\_spend\_mgmt.category\_manager\_admin

## Procedure

1.  Navigate to **All** &gt; **Load Data**.

    The **Load Data page appears**.

2.  In **Import set table**, select **Existing table**.

3.  From the **Import set table** list, select the Spend Category Stage \(sn\_spend\_mgmt\_category\_stage\) table.

4.  In **Source of the Import**, choose **File**.![Load Data page.](../image/create_load_data.png)

5.  Browse to the Excel template that was created in [Add spend category data in an Excel file](add-spend-data-spo.md).

6.  Enter the **Sheet number** of the Excel template that must be loaded into the staging table.

7.  Enter the **Header row** of the Excel template that must be loaded into the staging table.

8.  Select **Submit**.


## Result

The Excel template with spend category data is uploaded.

## What to do next

Run the transform to import the data from the Spend Category Stage table to the Spend Category primary table. For more information, see [Run transform to import spend category data into the Spend Category primary table](spend-category-run-trasnform.md).

**Related topics**  


[Spend and Savings Management](../concept/spo-spend-mgmt.md)

