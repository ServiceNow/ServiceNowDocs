---
title: Create an invoice line manually
description: Create invoice lines manually for an invoice when the invoice automation process doesn't capture this information from an incoming invoice.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/create-invoice-line.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, invoice capture, invoice processing, AP specialist]
breadcrumb: [Create an invoice manually, Work with invoices, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Create an invoice line manually

Create invoice lines manually for an invoice when the invoice automation process doesn't capture this information from an incoming invoice.

## Before you begin

Role required: sn\_ap\_apm.accounts\_payable\_specialist or sn\_ap\_apm.admin

## Procedure

1.  Navigate to **All** &gt; **All** &gt; **Accounts Payable Operations** &gt; **Accounts Payable Workspace**.

2.  Navigate to **Lists** &gt; **Invoices** &gt; **All Open Invoices**.

3.  In the Number column, select the link to the invoice that you want to create an invoice line for.

4.  Select the **Invoice lines** tab and select **New.**

5.  On the Create New Invoice Line form, fill in the fields.

    For a description of the field values, see [Create New Invoice Line form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-invoice-line-form.md).

6.  Select **Save**.


-   **[Invoice rejection modes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/invoice-rejection-modes.md)**  
Invoice rejection modes control how Accounts Payable Operations handles exceptions that require an invoice to be rejected, either automatically by the system or through manual review by an AP specialist.
-   **[Reject an invoice manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/reject-an-invoice-manually.md)**  
Review exceptions flagged for manual rejection and reject an invoice from the invoice case when AP specialist confirmation is required.
-   **[Credit memo](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/invoice-type-credit-memo.md)**  
Credit memo invoices in Accounts Payable Operations represent reductions or offsets in amounts payable to suppliers and can be created for both PO and Non-PO invoices, with the system identifying them based on specific indicators such as negative amounts.

**Parent Topic:**[Create an invoice manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-invoice.md)

