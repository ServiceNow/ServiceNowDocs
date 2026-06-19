---
title: Outbound invoice fields
description: Field descriptions and data types for the outbound invoice table used to transfer invoice details from Accounts Payable Operations to third-party applications through the integration framework.”
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/outbound-invoice-fields.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, invoice management, integration, invoice management]
breadcrumb: [Create New Invoice form, Create New Invoice Line form, Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Outbound invoice fields

Field descriptions and data types for the outbound invoice table used to transfer invoice details from Accounts Payable Operations to third-party applications through the integration framework.”

|Column|Description|Data type|
|------|-----------|---------|
|Supplier invoice number|The combination of supplier invoice number or supplier and ERP source and ERP invoice number|String|
|Business owner.Email|Name of the owner who owns the application from the business side|String|
|Amount invoiced \(Transaction currency\).amount|Charges added to the invoice|String|
|Amount invoiced \(Transaction currency\).currency|Charges added to the invoice|String|
|Discounts.amount|Reduction on the total amount incurred on the invoice|String|
|Legal Entity.ERP Source.Source|Stores organizational entities defined in the application|String|
|Type|Details about the invoice|Choice|
|Supplier|Name of the supplier|Reference|
|Supplier invoice number|Invoice number mentioned by the supplier|String|
|Purchase order|Binding contract between a buyer and a supplier that authorizes a purchasing transaction|Reference|
|Invoice date|The date on which the invoice is created.|String \(yyy-mm-dd\)|
|Payment terms|Conditions applied on the payment|Reference|
|Tax amount.amount|Tax rate applied on the invoice amount|String|
|Shipping. amount|Shipping charges incurred for the invoice|String|
|Subtotal.amount|Total amount of money to be paid to the supplier excluding tax and shipping charges.|String|
|Other charges.amount|Additional charges incurred on the invoice|String|
|Number|Unique business identifier associated with the business partner|String|
|Status|Current state of the invoice|Choice|
|Invoice date|Date on which the invoice was created|String \(yyyy-mm-dd\)|

-   **[Outbound invoice line fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/outbound-invoice-line-fields.md)**  
Field descriptions and data types for the Outbound invoice line \[sn\_spend\_intg\_outbound\_invoice\_line\] table used to transfer invoice line details from Accounts Payable Operations to third-party applications through the integration framework.

**Parent Topic:**[Create New Invoice form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-new-invoice-form.md)

