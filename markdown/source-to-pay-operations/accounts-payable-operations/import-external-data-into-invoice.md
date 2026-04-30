---
title: Import data into invoice
description: You can import bulk data through transform map using excel file.
locale: en-US
release: xanadu
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Accounts Payable Operations integration framework, Integrating APO with other applications, Accounts Payable Operations, Finance and Supply Chain]
---

# Import data into invoice

You can import bulk data through transform map using excel file.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Workspace**.

2.  View the inbound table sn\_spend\_intg\_imp\_invoice\_list.do.

3.  Right-click the column heading.

4.  Select **Import**.

    The **Import external data into Invoice Import** page appears. For more information on importing data through transform map, see [Run transform to update invoice data](run-transform.md).

    **Note:** Follow the same steps for invoice lines and invoice payment.

5.  Select if you want to **Insert** or **Update** data.

    By default, **Insert** is selected.

6.  Check the **Do you want to create an Excel template to enter data?** check box.

    1.  In **Create an Excel template file to enter data**, select the **Include all fields in the template** check box.

    2.  Click **Create Excel template**.

    3.  In **Upload the template file**, browse for the excel file in XLS format.

    4.  Click **Upload**.


## Result

Excel template is created and uploaded with mandatory invoice data.

