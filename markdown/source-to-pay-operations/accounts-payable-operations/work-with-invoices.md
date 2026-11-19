---
title: Work with invoices
description: Invoices are generated for a payment against a purchase order. The Accounts Payable Specialist \[sn\_ap\_apm.accounts\_payable\_specialist\] can access all the invoices and take required actions to process the invoices in Source-to-Pay Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/source-to-pay-operations/accounts-payable-operations/work-with-invoices.html
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Using Accounts Payable Invoice Processing, Using Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Work with invoices

Invoices are generated for a payment against a purchase order. The Accounts Payable Specialist \[sn\_ap\_apm.accounts\_payable\_specialist\] can access all the invoices and take required actions to process the invoices in Source-to-Pay Workspace.

Accounts Payable Operations integration with Document Intelligence automatically extracts data from the invoices that are received as an attachment via email, and creates the invoice records and the invoice line records. When the invoice is in certain states during automated invoice processing, manual intervention is required by the Accounts Payable Specialist to move the invoice to the next stage of processing.

**Note:** Accounts Payable Operations supports invoices of type **PO Invoice**, **Non-PO Invoice**, **Credit memo**.

The Accounts Payable Specialist can view the invoices by doing the following:

1.  Navigate to **Accounts Payable Operations** &gt; **Source-to-Pay Workspace**.
2.  Select the list icon \(\[Omitted image "cases-list-icon.png"\] Alt text: List icon\).
3.  Navigate to **Lists** &gt; **Invoices**.

## Invoice life cycle

The following figure illustrates the various statuses and sub-statuses that the invoice goes through during its life cycle, from its creation to approval.

\[Omitted image "invoice-lifecycle-apm.png"\] Alt text: Invoice life cycle

The following figure illustrates the various statuses and sub-statuses that the non-PO invoice goes through during its life cycle, from its creation to approval.

\[Omitted image "non-po-invoice.png"\] Alt text: Non-PO invoice lifecycle

The following figure illustrates the various statuses and sub-statuses that the credit memo invoice goes through during its life cycle, from its creation to approval.

\[Omitted image "credit-memo-lifecycle.png"\] Alt text: Credit memo life cycle

-   **[Create an invoice manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/accounts-payable-operations/create-invoice.md)**  
As an Accounts Payable Specialist, you can create an invoice manually from the Source-to-Pay Workspace when the automated invoice creation process is encountering issues or not available.
-   **[Update the purchase order on an invoice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/accounts-payable-operations/change-invoice-po-number.md)**  
If you find that the purchase order that is currently associated with an invoice is incorrect, you can associate the correct purchase order to the invoice.
-   **[View your invoices on Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/accounts-payable-operations/view-invoices-ec.md)**  
As a business owner, you can view all the invoices that you own on Employee Center.

**Parent Topic:**[Using Accounts Payable Invoice Processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/accounts-payable-operations/use-ap-invoice-processing.md)

**Related topics**  


[Invoice ingestion using Application programming interface \(API\)]()

[Rules based engine]()

[Invoice processing cases]()

[Invoice exceptions]()

[Tolerance Rules and Variances for invoices]()

[Invoice approvals]()

[View invoice documents in the Source-to-Pay Workspace]()

