---
title: Accounts Receivable \(AR\) invoice line table
description: The AR invoice line \(sn\_otc\_invoice\_line\) table stores the invoice line data.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Case Management for Invoice Operations, Case management, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Accounts Receivable \(AR\) invoice line table

The AR invoice line \(sn\_otc\_invoice\_line\) table stores the invoice line data.

## Accounts Receivable invoice line table

The following table lists the fields for AR invoice line \[sn\_otc\_invoice\_line\] table.

|Field|Data type|Description|
|-----|---------|-----------|
|Invoice Number|Reference to AR Invoice|Parent invoice number containing the invoice lines.|
|Invoice line quantity|Decimal|The number of items that have been invoiced in the line.|
|Line item invoice with tax|FX Currency|The total cost which is being billed for this good or service with tax.|
|Line item invoice without tax|FX Currency|The total cost which is being billed for this good or service without tax.|
|Description|String|Brief description of the invoice line.|
|Line unit price|Decimal|Unit price of the line item in the invoice.|
|Part Number|String|SKU number from the product catalog|
|Line Item Number|String|Invoice line number|
|Sales Order|Reference to Order|Sales order associated with the invoice|
|Sales Order Number|String|Sales order associated with the invoice|
|Sales Order line|Reference to Order Line Item|Sales order line associated with the invoice line.|
|Sales Order line Number|String|Sales order line associated with the invoice line|
|Shipping to Contact|Reference to Account Contact|The account contact to which the order on the invoice is shipped.|
|Shipping to Location|Reference to Location|Reference to the location to which the order on the invoice is shipped.|
|Ship to city|String|The city to which the order on the invoice is shipped.|
|Ship to country|Reference to Country|The country to which the order on the invoice is shipped.|
|Ship to state/province|String|The state to which the order on the invoice is shipped.|
|Ship to street|String|The street address to which the order on the invoice is shipped.|
|Ship to zip/postal code|String|The zip code to which this order is shipped.|
|Status|String|Status of the invoice line.|
|Tax amount|FX Currency|Tax amount for the invoice line item.|
|Tax code|Reference to Tax Code|Tax code of the invoice line.|
|Tax jurisdiction code|String|Tax jurisdiction code of the invoice line.|
|Tax rate decimal|Decimal|Tax rate % applied on the invoice line - Tax rate in decimal if tax code is not used.|
|Tax rate string|String|Tax rate % applied on the invoice line - Tax rate in string if tax code and decimal is not used.|
|Unit of Measure|Reference to Unit|Unit of Measure for the invoice line item quantity.|

