---
title: Invoice processing details
description: Field descriptions for the Invoice attributes form stored in the \[sn\_apm\_invoice\_attribute\] table, including invoice processing details such as approval status, exception handling, and matching errors.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/invoice-processing-form.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, invoice automation, AP automation, invoice processing]
breadcrumb: [Invoice processing case form, Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Invoice processing details

Field descriptions for the Invoice attributes form stored in the \[sn\_apm\_invoice\_attribute\] table, including invoice processing details such as approval status, exception handling, and matching errors.

|Tab|Description|
|---|-----------|
|Approval date|The date, in DD/MM/YYYY format, on which an invoice was approved for payment, either automatically or manually.|
|Auto approved|Indicates that the invoice was approved automatically without requiring manual Accounts Payable specialist review.|
|Created|The date and time the invoice was created in DD/MM/YYYY and HH:MM:SS format.|
|Created by|Name of the person who created the invoice.|
|Exceptions|Exception engine evaluates the invoice. A boolean value is set to true if the invoice gets stuck with exceptions, or otherwise it is set to false.|
|Extraction failed|Indicates that the automated invoice data extraction process encountered errors. When `true`, the invoice requires manual data entry.|
|Invoice|Name of the invoice.|
|Last exception check time|The date and time, in DD/MM/YYYY and HH:MM:SS format, when the exception engine last processed this invoice.|
|Manual review in ingestion|Indicates that the invoice was flagged for manual review during the ingestion process.|
|Matching error|Indicates that the invoice encountered the **PO matching error** state.|
|Rejected|Indicates that the invoice or line has been rejected and will not be processed for payment.|
|Suspected duplicate|Indicates that the invoice is suspected to be a duplicate of another invoice in the system. The value is set to true for invoices that run into the **Suspected duplicate** state, otherwise, it is false.|
|Sys\_id|Unique ID of the invoice processing detail record.|
|Tags|Invoice processing detail-related tags.|
|Tolerance applied|Indicates whether tolerance rules were applied so the invoice can proceed despite variances.|
|Updated|The date and time, in DD/MM/YYYY and HH:MM:SS format, the invoice processing detail is updated.|
|Updated by|Name of the person who updated the invoice processing detail record.|
|Updates|Integer value set if any updates are performed on the invoice processing detail record.|

**Parent Topic:**[Invoice processing case form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/invoice-processing-case-form.md)

