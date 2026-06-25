---
title: Invoice processing cases
description: Accounts Payable Operations integration with Document Intelligence automatically creates invoice processing cases from email attachments, with specialists manually creating or updating invoices when automation is unavailable or fails, and Accounts Payable Specialists use this process to ensure invoice data is complete and accurate for processing.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/working-with-ingestion-cases.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [APO, Accounts Payable Operations, invoice capture, invoice processing, DocIntel, Document Intelligence, AP case, integration, email ingestion]
breadcrumb: [Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Invoice processing cases

Accounts Payable Operations integration with Document Intelligence automatically creates invoice processing cases from email attachments, with specialists manually creating or updating invoices when automation is unavailable or fails, and Accounts Payable Specialists use this process to ensure invoice data is complete and accurate for processing.

By default, when an inbound email is received in Accounts Payable Operations integration with Document Intelligence, the invoice processing flow is triggered and an invoice case with a category of **Invoice automation** and sub-category of **Invoice processing** is created. For more information, see [Install Accounts Payable Operations integration with Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/apm-integration-docintel.md).

Frequently asked questions.

How do I activate orphan invoice processing?

Activate the `Start Invoice Processing for Orphan Invoices` flow in Flow Designer. This flow automatically picks up all PO and Non-PO invoice records in Draft status that don't have an associated invoice processing case and starts their processing. You only need this manual activation step if the flow was not already activated during installation.

-   **[Work on an invoice processing case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/work-manual-invoice-ingestion-case.md)**  
Perform manual actions to review, update, and resolve invoice processing issues during the invoice lifecycle.
-   **[Invoice ingestion process when Document Intelligence is unavailable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/invoice-ingest-docintel-unavailable.md)**  
When Document Intelligence is unavailable or not installed, Accounts Payable Operations creates an invoice processing case without generating an invoice record, requiring manual invoice creation.

**Parent Topic:**[Using Accounts Payable Invoice Processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/use-ap-invoice-processing.md)

**Related topics**  


[Invoice ingestion using Application programming interface \(API\)]()

[Rules based engine]()

[Work with invoices]()

[Invoice exceptions]()

[Tolerance Rules and Variances for invoices]()

[Invoice approvals]()

[View invoice documents in the Source-to-Pay Workspace]()

