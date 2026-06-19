---
title: Create an invoice manually
description: Manually create an invoice from the Source-to-Pay Workspace when the automated invoice creation process encounters issues or is unavailable.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/create-invoice.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations,, invoice management, integration, inbound integration,, outbound integration]
breadcrumb: [Work with invoices, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Create an invoice manually

Manually create an invoice from the Source-to-Pay Workspace when the automated invoice creation process encounters issues or is unavailable.

## Before you begin

Role required: sn\_ap\_apm.accounts\_payable\_specialist or sn\_ap\_apm.admin

## About this task

Invoices are created automatically by integration with Document Intelligence. However, you can also create invoices manually.

## Procedure

1.  Navigate to **All** &gt; **All** &gt; **Accounts Payable Operations** &gt; **Source-to-Pay Workspace**.

2.  Under Quick actions, select **Create New Invoice**.\[Omitted image "create-invoice-manually.png"\] Alt text: Create invoice manually

3.  On the Create New Invoice form, fill in the fields.

    For a description of the field values, see [Create New Invoice form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-new-invoice-form.md).

4.  Select **Save**.

    A new invoice is created in the Draft state, a new invoice case is created with a category of Invoice automation and sub-category of Invoice processing, and the new invoice is associated with the invoice case.

    For more information about working with an invoice processing case, see [Work on an invoice processing case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/work-manual-invoice-ingestion-case.md).


## What to do next

Create invoice lines for the invoice. For more information, see [Create an invoice line manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-invoice-line.md).

-   **[Create an invoice line manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-invoice-line.md)**  
Create invoice lines manually for an invoice when the invoice automation process doesn't capture this information from an incoming invoice.
-   **[Invoice cost allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/invoice-line-cost-allocation.md)**  
Cost allocation distributes invoice line costs across multiple cost centers or ledger accounts to ensure accurate financial reporting and proper expense tracking in Accounts Payable Operations.
-   **[Tax calculations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/tax-calculations-in-apo.md)**  
Tax calculations in Accounts Payable Operations validate supplier-provided taxes against system-calculated amounts to determine the final tax for invoices.

**Parent Topic:**[Work with invoices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/work-with-invoices.md)

