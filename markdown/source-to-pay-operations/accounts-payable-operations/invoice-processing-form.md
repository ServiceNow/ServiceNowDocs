---
title: Invoice processing details
description: Accounts Payable Specialists can use the Invoice processing detailed form to view the invoice details. Invoice processing detail is found in the the sn\_apm\_invoice\_attributetable.
locale: en-US
release: xanadu
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2023-10-09"
reading_time_minutes: 1
breadcrumb: [Invoice processing case form, Accounts Payable Operations reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Invoice processing details

Accounts Payable Specialists can use the Invoice processing detailed form to view the invoice details. Invoice processing detail is found in the the `sn_apm_invoice_attribute`table.

|Tab|Description|
|---|-----------|
|Approval date|Approved invoice date in DD/MM/YYYY format.|
|Auto approved|A boolean value is set to either true if the invoice is auto approved, or else it is set to false.|
|Created|Timestamp of the invoice created in DD/MM/YYYY and HH:MM:SS format.|
|Created by|Name of the person who created the invoice.|
|Exceptions|Exception engine evaluates the invoice. A boolean value is set to true if the invoice gets stuck with exceptions, or else it is set to false.|
|Extraction failed|A boolean value is set to true if any of the invoice fields fails during extraction, or else it is set to false.|
|Invoice|Name of the invoice.|
|Last exception check time|Timestamps of the last exception check performed on the invoice in DD/MM/YYYY and HH:MM:SS format.|
|Manual review in ingestion|The boolean value is set to true if invoice is manually submitted by Accounts Payable specialist instead of automated process, or else it is set to false.|
|Matching error|A boolean value is set to true for invoices that run into **PO matching error**state, or else it is set to false.|
|Rejected|A boolean value is set to true if the invoice is rejected by an approver, or else it is set to false.|
|Suspected duplicate|A boolean value is set to true for invoices that run into **Suspected duplicate** state, or else it is set to false.|
|Sys\_id|Unique ID of the invoice processing detail record.|
|Tags|Invoice processing detail-related tags.|
|Tolerance applied|A boolean value is set to true if any tolerance rule is applied on the invoice that helps prevents it from creating an exception, or else it is set to false.|
|Updated|Timestamp of the invoice processing detail updated in DD/MM/YYYY and HH:MM:SS format.|
|Updated by|Name of the person who updates the invoice processing detail record.|
|Updates|Integer value set if any updates are performed on the invoice processing detail record.|

**Parent Topic:**[Invoice processing case form](invoice-processing-case-form.md)

