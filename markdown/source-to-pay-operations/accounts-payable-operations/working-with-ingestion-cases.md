---
title: Invoice processing cases
description: Typically, Accounts Payable Operations integration with Document Intelligence automatically creates the invoice processing case by extracting data from the invoice that you receive as an attachment via email. However, the Accounts Payable Specialist may need to manually create a new invoice or update details of a partially created invoice in situations where the automated invoice creation process encounters issues or is not available.
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Invoice processing cases

Typically, Accounts Payable Operations integration with Document Intelligence automatically creates the invoice processing case by extracting data from the invoice that you receive as an attachment via email. However, the Accounts Payable Specialist may need to manually create a new invoice or update details of a partially created invoice in situations where the automated invoice creation process encounters issues or is not available.

By default, when an inbound email is received in Accounts Payable Operations integration with Document Intelligence, the invoice processing flow is triggered and an invoice case with a category of **Invoice automation** and sub-category of **Invoice processing** is created. For more information, see [Install Accounts Payable Operations integration with Document Intelligence](apm-integration-docintel.md).

## Invoice processing case life cycle

The following figure illustrates the various states that the Invoice processing case goes through during its life cycle, from its creation to closure.

![Invoice processing case life cycle](../image/ingestion-case-lifecycle-apm.png "Manual invoice ingestion case life cycle")

|State|Description|
|-----|-----------|
|New|The case is created.|
|Assigned|The case is assigned.|
|Work in progress|The case is being worked on.|
|Closed complete|The case moves to this state after the invoice approval request is approved by the approver or after the invoice is auto-approved by the approval engine.|
|Closed incomplete|The case moves to this state when the invoice is in the Suspected duplicate state and the Accounts Payable Specialist selects the **Confirm duplicate** option.|
|Canceled|The case is canceled because it was created in error or is no longer required.|

-   **[Work on an invoice processing case](../task/work-manual-invoice-ingestion-case.md)**  
Perform different manual actions to process an invoice.
-   **[Invoice ingestion process when Document Intelligence is unavailable](invoice-ingest-docintel-unavailable.md)**  
When Document Intelligence goes down or when Document Intelligence itself is not installed, and if you receive an invoice document via email, an invoice processing case is created but an invoice record is not created.

**Parent Topic:**[Using Accounts Payable Invoice Processing](use-ap-invoice-processing.md)

**Related topics**  


[Invoice ingestion using Application programming interface \(API\)](invoice-ingestion-using-api.md)

[Rules based engine](rules-based-engine.md)

[Work with invoices](work-with-invoices.md)

[Invoice exceptions](work-with-invoice-exceptions.md)

[Tolerance Rules and Variances for invoices](tolerance-rules-and-variance.md)

[Invoice approvals](invoice-approvals.md)

[View invoice documents in the Source-to-Pay Workspace](../task/view-invoice-attachment.md)

