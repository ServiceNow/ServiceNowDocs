---
title: Working with inbound invoice
description: Create invoice and invoice lines originating from different ERP sources using an integration framework.
locale: en-US
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Accounts Payable Operations integration framework, Integrate, Accounts Payable Operations, Finance and Supply Chain]
---

# Working with inbound invoice

Create invoice and invoice lines originating from different ERP sources using an integration framework.

## Before you begin

-   [Import data into invoice](import-external-data-into-invoice.md)
-   [Load invoice data](load-data.md)
-   [Run transform to update invoice data](run-transform.md)

Role required: sn\_spend\_intg\_admin or sn\_spend\_intg\_procurement\_integrator

## Procedure

1.  Open `sn_spend_intg_imp_invoice_list.do` staging table.

    The **Invoice Imports** lists the inbound invoice columns. For more information on the inbound fields, refer [Inbound Invoice Fields](../reference/inbound-invoice-fields.md).

    **Note:** If the required inbound fields are validated and entered, then the **Status** is set to inserted.

2.  Open any inbound record with **Status** as **Inserted**.

3.  Navigate to **Import Set** &gt; **Target record**.

4.  Select **Open Record**.

    Invoice record is created in the **Draft** state and the scheduled job is run every thirty minutes. If the required fields on the invoice are filled, and no exceptions are found, then the invoice is auto set to **Approved** status.


## Result

Invoice and invoice lines are created using integration framework.

