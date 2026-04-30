---
title: Run transform to update invoice data
description: Use transform map and run transform to map the invoice fields from the import set into target tables in Accounts Payable Operations.
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Load invoice data, Import data into invoice, Accounts Payable Operations integration framework, Integrate, Accounts Payable Operations, Finance and Supply Chain]
---

# Run transform to update invoice data

Use transform map and run transform to map the invoice fields from the import set into target tables in Accounts Payable Operations.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Load Data** &gt; **Run Transform**.

    The **Specify Import set and Transform map** screen appears. In the **Import set**, the staging table you selected from [Load invoice data](load-data.md) is auto populated. In **Selected maps, run in order** area, the target invoice table to be mapped in Accounts Payable Operations is auto-populated and selected by default.

2.  Click **Transform**.


## Result

The invoice fields from the import set is mapped to `sn_shop_invoice` table.

