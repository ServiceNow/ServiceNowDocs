---
title: Load invoice data
description: Load bulk invoice data from an Excel template into the Accounts Payable Operations invoice import staging table sn\_spend\_intg\_imp\_invoice.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/load-data.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, invoice management, staging table]
breadcrumb: [Import data into invoice, Accounts Payable Operations integration framework, Integrate, Accounts Payable Operations, Finance and Supply Chain]
---

# Load invoice data

Load bulk invoice data from an Excel template into the Accounts Payable Operations invoice import staging table `sn_spend_intg_imp_invoice`.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Load Data**.

    The **Load Data page appears**.

2.  In **Import set table**, choose **Existing table** option.

3.  Choose the invoice table from the drop-down list.

4.  In **Source of the Import**, choose **File**.

5.  Browse the excel template that was created from [Import data into invoice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/import-external-data-into-invoice.md).

6.  Enter the **Sheet number** of the excel template that needs to be loaded into the staging table.

7.  Enter the **Header row** of the excel template that needs to be loaded into the staging table.

8.  Click **Submit**.


## Result

The invoice data from the excel template is processed successfully.

