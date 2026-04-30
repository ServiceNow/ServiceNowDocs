---
title: Example of ERP posting error workflow
description: The ERP posting error example shows the different stages involved in closing integration issues using the error task.
locale: en-US
release: xanadu
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integration errors, Accounts Payable Operations integration framework, Integrating APO with other applications, Accounts Payable Operations, Finance and Supply Chain]
---

# Example of ERP posting error workflow

The ERP posting error example shows the different stages involved in closing integration issues using the error task.

## Before you begin

Role required: Accounts Payable admin

## Procedure

1.  Navigate to **All** &gt; **Source-to-Pay Workspace** &gt; **Accounts Payable Operations**.

    The Accounts Payable Operations landing page appears.

2.  Select **ERP Posting error**.

    The **ERP Posting error invoices** page lists the invoice cases with **ERP integration status** as **Failed**.

3.  Select an invoice case.

    The **Pay invoice** playbook card auto-opens **Review integration errors** card. An error message displays the reason for integration failure. Example: There was an integration error for this invoice. Complete the tasks to ensure that the invoice details are correct.

4.  Select the error task in **Review integration errors** page.

    The **Review integration error for XXXXX** form opens. Review the error description which explains the reason for integration failure. Example: Network failure. For more information about the ERP posting error task, see [ERP Posting error form](../reference/erp-posting-erorr-form.md).

5.  Open the **Invoice header** form and edit the invoice fields with appropriate details.

6.  Open the **Invoice Lines** form and edit the invoice fields with appropriate details.

7.  Select **Save**.

    The changes to the forms are saved.

8.  Select **Send to ERP**.

9.  As an alternate step, you can also open the playbook of invoice processing case and select**Send to ERP**.

    ln the outbound table, an invoice with status **New** is created. The integration status in the outbound invoice is updated to **Processed**. In case of cost allocation records, when an invoice is submitted for approval and if the ERP fails to process the invoice, then an integration task is created. Accounts Payable specialists review the integration error task and manually process the invoice using **Send to ERP**. The outbound staging record displays the invoice lines, tax lines and cost allocation details.

10. In the invoice **Details** tab, the **Status** is auto-updated as **Pending payment**.

11. Select **Review Payments**.

    For more information on payment fields, see [Inbound invoice payment fields](../reference/inbound-invoice-payment-fields.md).


## Result

The ERP integration error tasks are closed and the invoice is successfully processed for payment.

