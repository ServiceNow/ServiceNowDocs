---
title: Accounts Receivable \(AR\) invoice table
description: The AR invoice \(sn\_otc\_invoice\) table stores the invoice data.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Case Management for Invoice Operations, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Accounts Receivable \(AR\) invoice table

The AR invoice \(sn\_otc\_invoice\) table stores the invoice data.

## Accounts Receivable invoice table

The following table lists the fields for AR invoice \[sn\_otc\_invoice\] table.

|Field|Data type|Description|
|-----|---------|-----------|
|Account|Reference to Account|Customer in the business-to-business \(B2B\) business model.|
|Amount invoiced with tax \(Reporting currency\)|FX Currency|Total amount to be paid to the supplier including tax and shipping charges. This amount is displayed in reporting currency.|
|Amount invoiced with tax \(Transaction currency\)|FX Currency|Total amount to be paid to the supplier including tax and shipping charges. This amount is displayed in transactional currency.|
|Amount invoiced without tax \(Reporting currency\)|FX Currency|Total amount to be paid to the supplier excluding tax and shipping charges. This amount is displayed in reporting currency.|
|Amount invoiced without tax \(Transaction currency\)|FX Currency|Total amount to be paid to the supplier excluding tax and shipping charges. This amount is displayed in transactional currency.|
|Billing Contact|Reference to Account Contact|The account contact to which the invoice is sent.|
|Billing Location|Reference Location|Reference to the location to which the invoice is sent.|
|Bill to city|String|The city to which the invoice is sent.|
|Bill to country|Reference to Country|The country to which the invoice is sent.|
|Bill to state/province|String|The state to which the invoice is sent.|
|Bill to street|String|The street address to which the invoice is sent.|
|Bill to ZIP/postal code|String|The zip code to which this invoice is sent.|
|Business owner|Reference to User|A group who owns the invoice.|
|Consumer|Reference to Consumer|Customer in the business-to-consumer \(B2C\) business model.|
|Created|Date/Time|Date on which this invoice is created.|
|Created by|String|Person who created the invoice.|
|Tax Code|Reference to Tax Code|The tax code levied on the total invoice amount.|
|Tax Jurisdiction Code|String|The tax code jurisdiction to which you must pay the tax.|
|Discount \(%\)|Decimal|Discount % for the discounts amount.|
|Discount due date|Date|Date by which you must make payment for the discounts to be applicable.|
|Discounts Amount|FX Currency|The discount applied on the invoice amount.|
|Due date|Date|Date by when you must make the payment.|
|Early payment discount amount|FX Currency|The discount applied on the total invoice amount on early payment.|
|ERP number|String|Unique number generated within the ERP system for the invoice.This field is applicable when there’s an ERP integration. The value is populated after the invoice is posted in the ERP system through the integration.|
|ERP posting date|Date|Date on which the invoice is posted in the ERP system.|
|Has changed|True/False|Denotes if the invoice has changed.|
|Invoice date|Date|Date on which this invoice is created.|
|Invoice source|String|Name of the application associated with the invoice from where it is sourced.|
|Number|String|An auto-generated number that uniquely identifies the invoice.|
|Other charges|FX Currency|Additional charges incurred on the invoice.|
|Parent invoice|Reference to AR Invoice|Original invoice|
|Payment date|Date|The date by when you must make the payment.|
|Payment terms|Reference to payment terms|Conditions applied on the payment|
|Remit to Contact|Reference to Account Contact|The account contacted to which the payment is made.|
|Remit to Location|Reference to Location|Reference to the location to which the payment is made.|
|Remit to city|String|The city to which the payment is made.|
|Remit to country|Reference to Country|The country to which the payment is made.|
|Remit to state/province|String|The state to which the payment is made.|
|Remit to street|String|The street address to which the payment is made.|
|Remit to zip/postal code|String|The zip code to which this payment is made.|
|Requires acknowledgment|True/False|Invoice requires acknowledgment of receipt from recipient|
|Sales Order|Reference to Order|Sales order associated with the invoice.|
|Sales order number|String|Sales order associated with the invoice.|
|Customer tax id|String|The tax ID of the customer|
|Customer Contact|Reference to Account Contact|The account contact of the customer for the invoice.|
|Customer Location|Reference to Location|Reference to the customer location for the invoice.|
|Customer city|String|The city of the customer for the invoice.|
|Customer country|Reference to Country|The country of the customer for the invoice.|
|Customer state/province|String|The country of the customer for the invoice.|
|Customer street|String|The street address of the customer for the invoice.|
|Customer zip/postal code|String|The zip code of the customer for the invoice.|
|Shipping from Location|Reference to Location|Reference to the location from which the order on the invoice is shipped.|
|Ship from city|String|The city from which the order on the invoice is shipped.|
|Ship from country|Reference to Country|The country from which the order on the invoice is shipped.|
|Ship from state/province|String|The state from which the order on the invoice is shipped.|
|Ship from street|String|The street address from which the order on the invoice is shipped.|
|Ship from zip/postal code|String|The zip code from which this order is shipped.|
|Shipping to Contact|Reference to Account Contact|The account contacted to which the order on the invoice is shipped.|
|Shipping to Location|Reference to Location|Reference to the location to which the order on the invoice is shipped.|
|Ship to city|String|The city to which the order on the invoice is shipped.|
|Ship to country|Reference to Country|The country to which the order on the invoice is shipped.|
|Ship to state/province|String|The state to which the order on the invoice is shipped.|
|Ship to street|String|The street address to which the order on the invoice is shipped.|
|Ship to zip/postal code|String|The zip code to which this order is shipped.|
|Shipping Charges|FX Currency|Shipping charges incurred for the invoice.|
|Short description|String|Brief description about the invoice.|
|Status|String|Current state of the invoice.|
|Submitted by|Reference to User|Person who submitted the invoice.|
|Subtotal|FX Currency|The total amount from all the invoice lines without tax and shipping charges.|
|Supplier|Reference to Supplier|Supplier who delivers the product or service.|
|Supplier tax id|String|The tax ID of the supplier.|
|Tax amount|FX Currency|Tax applied on the invoice amount.|
|Tax rate decimal|Decimal|Tax rate % applied on the invoice - Tax rate in decimal if tax code is not used.|
|Tax Rate String|String|Tax rate % applied on the invoice - Tax rate in string if tax code and decimal is not used|
|Type|String|The type of invoice debit or credit.|

