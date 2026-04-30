---
title: Outbound invoice fields
description: The outbound invoice table transfers the invoice details from ServiceNow to third party applications through integration framework.
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create New Invoice form, Create New Invoice Line form, Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Outbound invoice fields

The outbound invoice table transfers the invoice details from ServiceNow® to third party applications through integration framework.

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

-   **[Outbound invoice line fields](outbound-invoice-line-fields.md)**  
The Outbound invoice line table is the transfers the invoice line details table from ServiceNow® to third party application through integration framework.

**Parent Topic:**[Create New Invoice form](create-new-invoice-form.md)

