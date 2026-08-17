---
title: Invoice processing cases
description: Integrate Accounts Payable Operations integration with Document Intelligence to auto-create invoice cases and verify data accuracy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/working-with-ingestion-cases.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [APO, Accounts Payable Operations, invoice automation, invoice processing, DocIntel, Document Intelligence, Flow Designer, email ingestion, Orphan Invoice flow]
breadcrumb: [Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Invoice processing cases

Integrate Accounts Payable Operations integration with Document Intelligence to auto-create invoice cases and verify data accuracy.

By default, when an inbound email is received in Accounts Payable Operations integration with Document Intelligence, the invoice processing flow is triggered and an invoice case with a category of **Invoice automation** and sub-category of **Invoice processing** is created. For more information, see [Install Accounts Payable Operations integration with Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/apm-integration-docintel.md).

Frequently asked questions.

How do I activate orphan invoice processing?

Activate the Start Invoice Processing for Orphan Invoice flow in Flow Designer. This flow automatically picks up all PO and Non-PO invoice records in Draft status that don't have an associated invoice processing case and starts their processing. You only need this manual activation step if the flow was not already activated during installation.

-   **[Work on an invoice processing case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/work-manual-invoice-ingestion-case.md)**  
Perform manual actions to review, update, and resolve invoice processing issues during the invoice lifecycle.
-   **[Invoice ingestion process when Document Intelligence is unavailable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/invoice-ingest-docintel-unavailable.md)**  
When Document Intelligence is unavailable, Accounts Payable Operations requires manual invoice creation for cases.

**Parent Topic:**[Using Accounts Payable Invoice Processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/use-ap-invoice-processing.md)

**Related topics**  


[Invoice ingestion using the AP Invoice API]()

[Rules based engine]()

[Invoice processing]()

[Invoice exceptions]()

[Tolerance rules and variances for invoices]()

[Invoice approvals]()

[View invoice documents in the Source-to-Pay Workspace]()

