---
title: Credit memo
description: Credit memo invoices in Accounts Payable Operations represent reductions or offsets in amounts payable to suppliers and can be created for both PO and Non-PO invoices, with the system identifying them based on specific indicators such as negative amounts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/invoice-type-credit-memo.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, invoice management, invoice automation, AP automation]
breadcrumb: [Create an invoice line manually, Create an invoice manually, Work with invoices, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Credit memo

Credit memo invoices in Accounts Payable Operations represent reductions or offsets in amounts payable to suppliers and can be created for both PO and Non-PO invoices, with the system identifying them based on specific indicators such as negative amounts.

When an invoice is ingested into the Accounts Payable Operations application recognizes if the invoice received through various channels is of type credit memo. A credit memo is a document issued between a supplier and the buyer when there’s a reduction or any offset in the amount payable to the supplier. Credit memo is also applicable for any goods or services that the buyer owes to a seller. In some cases, if the buyer hasn’t paid the seller, the credit memo can be used as an offset for an invoice generated in the past or future. For an invoice to be recognized as a credit memo:

-   The credit memo invoice must contain one of the following:
    -   Original invoice
    -   Original invoice number
    -   Purchase order
-   Credit memos issued for purchase order or invoice number must match with purchase order lines and invoice lines
-   Invoice contains negative amount fields

For more information on creating invoice, see [Create New Invoice form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-new-invoice-form.md).

For more information on invoices ingested using document intelligence, see [Invoice data transformation logic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/invoice-data-trans-logic.md).

**Parent Topic:**[Create an invoice line manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-invoice-line.md)

