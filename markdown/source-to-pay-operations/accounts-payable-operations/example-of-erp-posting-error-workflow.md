---
title: Example of ERP posting error workflow
description: Follow a step-by-step example of how to close ERP posting integration errors using the error task workflow in Accounts Payable Operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/example-of-erp-posting-error-workflow.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, ERP integration, invoice automation]
breadcrumb: [Integration errors, Accounts Payable Operations integration framework, Integrate, Accounts Payable Operations, Finance and Supply Chain]
---

# Example of ERP posting error workflow

Follow a step-by-step example of how to close ERP posting integration errors using the error task workflow in Accounts Payable Operations.

## Before you begin

Role required: Accounts Payable admin

## Procedure

1.  Navigate to **All** &gt; **Source-to-Pay Workspace** &gt; **Accounts Payable Operations**.

    The Accounts Payable Operations landing page appears.

2.  Click **ERP Posting error**.

    The **ERP Posting error invoices** page lists the invoice cases with **ERP integration status** as **Failed**.

3.  Click an invoice case.

    The **Pay invoice** playbook card auto-opens **Review integration errors** card. An error message displays the reason for integration failure. Example: There was an integration error for this invoice. Complete the tasks to ensure the invoice details are correct.

4.  Click the error task in **Review integration errors** page.

    The **Review integration error for XXXXX** form opens. Review the error description which explains the reason for integration failure. Example: Network failure. For more information about the ERP posting error task, see [ERP Posting error form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/erp-posting-erorr-form.md).

5.  Open the **Invoice header** form and edit the invoice fields with appropriate details.

6.  Open the **Invoice Lines** form and edit the invoice fields with appropriate details.

7.  Click **Save**.

    The changes to the forms are saved.

8.  Click **Send to ERP**.

    You can also open the playbook of invoice processing case and select send to ERP. ln the outbound table, an invoice with status **New** is created. The integration status in the outbound invoice is updated to **Processed**.

9.  In the invoice **Details** tab, the **Status** is auto-updated as **Pending payment**.

10. Click **Review Payments**.

    For more information on payment fields, see [Inbound invoice payment fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/inbound-invoice-payment-fields.md).

    The ERP integration error tasks are closed and the invoice is successfully processed for payment.


