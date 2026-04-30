---
title: Invoice ingestion using Application programming interface \(API\)
description: The invoice ingestion API enables customers to ingest bulk AP invoices from external systems such as supplier billing systems, buyer network, and OCR solutions, supplier networks into APO. The supported payload formats are cXML, JSON and XML.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Using Accounts Payable Invoice Processing, Using Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Invoice ingestion using Application programming interface \(API\)

The invoice ingestion API enables customers to ingest bulk AP invoices from external systems such as supplier billing systems, buyer network, and OCR solutions, supplier networks into APO. The supported payload formats are cXML, JSON and XML.

The system property \[ap.invoice.create.api.record\_limit\] enables users to set the maximum number of invoices that can be processed in a batch using the AP invoice create API.

The Rate limit AP invoice xml defines the maximum number of API calls invoked by external systems according to hour.

The APO application verifies that users have valid authorization to access the APIs.

Look up logic for reference fields is enhanced for invoices ingested via APIs and integration. The reference fields are:

-   Purchase order
-   Legal entity
-   Currency field
-   Country
-   Line quantity
-   Line unit price

For more information on the AP invoice API, see [AP Invoice API Developer Guide](https://www.servicenow.com/docs/access?context=apInvoice-dev-guide&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

**Parent Topic:**[Using Accounts Payable Invoice Processing](use-ap-invoice-processing.md)

**Related topics**  


[Rules based engine](rules-based-engine.md)

[Work with invoices](work-with-invoices.md)

[Invoice processing cases](working-with-ingestion-cases.md)

[Invoice exceptions](work-with-invoice-exceptions.md)

[Tolerance Rules and Variances for invoices](tolerance-rules-and-variance.md)

[Invoice approvals](invoice-approvals.md)

[View invoice documents in the Source-to-Pay Workspace](../task/view-invoice-attachment.md)

