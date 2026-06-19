---
title: Import data into invoice
description: Import bulk invoice data into Accounts Payable Operations using a transform map and Excel file.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/import-external-data-into-invoice.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, invoice management, invoice automation]
breadcrumb: [Accounts Payable Operations integration framework, Integrate, Accounts Payable Operations, Finance and Supply Chain]
---

# Import data into invoice

Import bulk invoice data into Accounts Payable Operations using a transform map and Excel file.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Workspace**.

2.  View the inbound table `sn_spend_intg_imp_invoice_list.do`.

3.  Right-click the column heading.

4.  Select **Import**.

    The **Import external data into Invoice Import** page appears. For more information on importing data through transform map, see [Run transform to update invoice data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/run-transform.md).

    **Note:** Follow the same steps for invoice lines and invoice payment.

5.  Select if you want to **Insert** or **Update** data.

    By default, **Insert** is selected.

6.  Check the **Do you want to create an Excel template to enter data?** check box.

    1.  In the Create an Excel template file to enter data dialog box, select the **Include all fields in the template** check box.

    2.  Click **Create Excel template**.

    3.  In **Upload the template file**, browse for the excel file in XLS format.

    4.  Click **Upload**.


## Result

Excel template is created and uploaded with mandatory invoice data.

