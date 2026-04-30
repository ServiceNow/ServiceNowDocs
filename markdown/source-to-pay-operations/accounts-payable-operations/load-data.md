---
title: Load invoice data
description: Load the invoice data from the excel template into the sn\_spend\_intg\_imp\_invoice staging table.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Import data into invoice, Accounts Payable Operations integration framework, Integrating APO with other applications, Accounts Payable Operations, Finance and Supply Chain]
---

# Load invoice data

Load the invoice data from the excel template into the `sn_spend_intg_imp_invoice` staging table.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Load Data**.

    The **Load Data page appears**.

2.  In **Import set table**, choose **Existing table** option.

3.  Choose the invoice table from the drop-down list.

4.  In **Source of the Import**, choose **File**.

5.  Browse the excel template that was created from [Import data into invoice](import-external-data-into-invoice.md).

6.  Enter the **Sheet number** of the excel template that needs to be loaded into the staging table.

7.  Enter the **Header row** of the excel template that needs to be loaded into the staging table.

8.  Click **Submit**.


## Result

The invoice data from the excel template is processed successfully.

