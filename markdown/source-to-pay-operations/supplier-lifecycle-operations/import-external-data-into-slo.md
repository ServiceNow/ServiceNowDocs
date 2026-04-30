---
title: Add supplier inbound data in an Excel file
description: You can import supplier inbound table data in an Excel file.
locale: en-US
release: yokohama
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Supplier Lifecycle Operations integration framework, Integrating Supplier Lifecycle Operations with other applications, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Add supplier inbound data in an Excel file

You can import supplier inbound table data in an Excel file.

## Before you begin

Role required: admin

## Procedure

1.  Select **All**.

2.  In the navigation filter, do one of the following:

    -   To see the list of columns in the supplier location inbound table, enter **sn\_fcms\_intg\_supplier\_location\_inbound\_list.do**.
    -   To see the list of columns in the supplier contact inbound table, enter **sn\_fcms\_intg\_supplier\_contact\_inbound\_list.do**.
    -   To see the list of columns in the supplier payment inbound table, enter **sn\_fcms\_intg\_supplier\_payment\_inbound\_stage\_list.do**.
    -   To see the list of columns in the supplier payment inbound table, enter **sn\_fcms\_intg\_supplier\_legal\_entity\_list.do**.
3.  Right-click any column heading and select **Export** &gt; **.xlsx**.

4.  Select **Download** to save the spreadsheet on your local system.


## Result

Depending on the supplier inbound table you selected, an Excel template is created with the mandatory columns for supplier location, supplier contacts, or supplier payment information. Use this Excel spreadsheet to enter the supplier data that you want to import and store into the SLO inbound staging tables.

## What to do next

Load the supplier data from the excel template into the supplier inbound​ staging tables. For more information, see [Load supplier data](load-supplier-data.md).

**Parent Topic:**[Supplier Lifecycle Operations integration framework](../concept/slo-int-framework.md)

