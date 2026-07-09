---
title: Create an invoice manually
description: As an Accounts Payable Specialist, you can create an invoice manually from the Source-to-Pay Workspace when the automated invoice creation process is encountering issues or not available.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/accounts-payable-operations/create-invoice.html
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Work with invoices, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Create an invoice manually

As an Accounts Payable Specialist, you can create an invoice manually from the Source-to-Pay Workspace when the automated invoice creation process is encountering issues or not available.

## Before you begin

Role required: sn\_ap\_apm.accounts\_payable\_specialist or sn\_ap\_apm.admin

## About this task

Invoices are created automatically by integration with Document Intelligence. However, you can also create invoices manually.

## Procedure

1.  Navigate to **All** &gt; **All** &gt; **Accounts Payable Operations** &gt; **Source-to-Pay Workspace**.

2.  Under Quick actions, select **Create New Invoice**.\[Omitted image "create-invoice-manually.png"\] Alt text: Create invoice manually

3.  On the Create New Invoice form, fill in the fields.

    For a description of the field values, see [Create New Invoice form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/create-new-invoice-form.md).

4.  Select **Save**.

    A new invoice is created in the Draft state, a new invoice case is created with a category of Invoice automation and sub-category of Invoice processing, and the new invoice is associated with the invoice case.

    For more information about working with an invoice processing case, see [Work on an invoice processing case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/work-manual-invoice-ingestion-case.md).


## Result

The invoice is created manually from the Source-to-Pay Workspace.

## What to do next

Create invoice lines for the invoice. For more information, see [Create an invoice line manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/create-invoice-line.md).

-   **[Create an invoice line manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/create-invoice-line.md)**  
Create invoice lines manually for an invoice when the invoice automation process doesn't capture this information from an incoming invoice.
-   **[Invoice cost allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/invoice-line-cost-allocation.md)**  
Cost allocation is a process of identifying and allocating the costs across different cost centers or ledger accounts. Accounts Payable specialists allocate invoice line cost across multiple cost centers or ledger accounts for accurate cost analysis and invoice processing.
-   **[Tax calculations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/tax-calculations-in-apo.md)**  
Calculate the final tax for an invoice based on the tax type and the tax tolerance variance.

**Parent Topic:**[Work with invoices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/work-with-invoices.md)

**Related topics**  


[Accounts Payable Invoice Processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/acc-pay-invoice-processing.md)

[Invoice Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/acc-pay-case-mgmt-overview.md)

[Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/acc-pay-workspace.md)

[Accounts Payable Operations integration with Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/apo-docintel-integration.md)

[Using Now Assist for Accounts Payable Operations \(APO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/using-now-assist-apo.md)

[Using Supplier Collaboration Portal in APO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/using-supplier-collaboration-portal.md)

[Invoice processing cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/working-with-ingestion-cases.md)

