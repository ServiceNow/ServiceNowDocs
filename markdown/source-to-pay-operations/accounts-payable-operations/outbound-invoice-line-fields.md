---
title: Outbound invoice line fields
description: Field descriptions and data types for the Outbound invoice line \[sn\_spend\_intg\_outbound\_invoice\_line\] table used to transfer invoice line details from Accounts Payable Operations to third-party applications through the integration framework.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/outbound-invoice-line-fields.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, invoice management, integration, outbound integration]
breadcrumb: [Outbound invoice fields, Create New Invoice form, Create New Invoice Line form, Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Outbound invoice line fields

Field descriptions and data types for the Outbound invoice line \[sn\_spend\_intg\_outbound\_invoice\_line\] table used to transfer invoice line details from Accounts Payable Operations to third-party applications through the integration framework.

|Column|Description|Data type|
|------|-----------|---------|
|Line description|Description of the invoice line|String|
|Purchase order line|Information of the individual lines under a purchase order line or a sourcing request for the referenced supplier|Reference|
|Invoice line quantity|The number of items that have been invoiced|String|
|Line unit price|Unit price of the line item in the invoice|String|
|Ledger account|Displays General Ledger Account|Reference|
|Tax amount.amount|Tax rate applied on the invoice amount|String|
|Subtotal.amount|Total amount of money to be paid to the supplier excluding tax and shipping charges.|String|
|Cost center|Represent business entity to which costs can be allocated|Reference|
|Status|Current state of the invoice|String|
|Invoice.Legal entity. ERP source|Stores organizational entities defined in the application|String|
|ERP line number|Displays the ERP number at the line item level|String|
|Invoice|Transaction record used to track purchase between shopper and supplier|Reference|
|Number|The number in the invoice|String|
|Status|Status of an invoice|Choice|
|Line amount.invoiced amount|The total amount for the invoice line|String|

**Parent Topic:**[Outbound invoice fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/outbound-invoice-fields.md)

