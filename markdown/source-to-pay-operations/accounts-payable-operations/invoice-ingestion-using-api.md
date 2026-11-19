---
title: Invoice ingestion using the AP Invoice API
description: The AP Invoice API enables bulk import of AP invoices from external systems, such as supplier billing platforms and OCR solutions, into Accounts Payable Operations using cXML, JSON, or XML.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/accounts-payable-operations/invoice-ingestion-using-api.html
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [APO, Accounts Payable Operations, invoice processing, invoice ingestion, AP case, email ingestion]
breadcrumb: [Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Invoice ingestion using the AP Invoice API

The AP Invoice API enables bulk import of AP invoices from external systems, such as supplier billing platforms and OCR solutions, into Accounts Payable Operations using cXML, JSON, or XML.

Invoice ingestion via API requires the Accounts Payable Invoice Processing \(com.sn\_ap\_apm\) and Source-to-Pay Integration Framework \(sn\_spend\_intg\) applications, which are available on the ServiceNow Store.

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

For more information about the AP Invoice API, see:

-   [AP Invoice API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/ap-invoice-api.md)
-   [AP Invoice API Developer Guide](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/developer-guides/apInvoice-dev-guide.md)

**Parent Topic:**[Using Accounts Payable Invoice Processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/use-ap-invoice-processing.md)

**Related topics**  


[Rules based engine]()

[Work with invoices]()

[Invoice processing cases]()

[Invoice exceptions]()

[Tolerance Rules and Variances for invoices]()

[Invoice approvals]()

[View invoice documents in the Source-to-Pay Workspace]()

