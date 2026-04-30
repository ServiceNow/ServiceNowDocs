---
title: Outbound invoice line fields
description: The Outbound invoice line table is the transfers the invoice line details table from ServiceNow to third party application through integration framework.
locale: en-US
release: xanadu
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Outbound invoice fields, Create New Invoice form, Create New Invoice Line form, Accounts Payable Operations reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Outbound invoice line fields

The Outbound invoice line table is the transfers the invoice line details table from ServiceNow® to third party application through integration framework.

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

**Parent Topic:**[Outbound invoice fields](outbound-invoice-fields.md)

