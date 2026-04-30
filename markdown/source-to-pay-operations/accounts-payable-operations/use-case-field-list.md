---
title: List of invoice and invoice line fields included in the use case for Accounts Payable Operations integration with Document Intelligence
description: The DO NOT USE - Invoice Processing use case includes the following set of invoice and invoice line fields from which to extract information from your invoice documents.
locale: en-US
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Invoice Processing use case, Install Accounts Payable Operations integration with Document Intelligence, Configure, Accounts Payable Operations, Finance and Supply Chain]
---

# List of invoice and invoice line fields included in the use case for Accounts Payable Operations integration with Document Intelligence

The **DO NOT USE - Invoice Processing** use case includes the following set of invoice and invoice line fields from which to extract information from your invoice documents.

|Field|Description|
|-----|-----------|
|Invoice Fields|
|Supplier invoice number|The invoice number of the supplier invoice.|
|Supplier|Supplier who delivers the product or service.|
|Supplier tax id|The tax ID of the supplier.|
|Invoice date|Date on which this invoice is created.|
|Purchase order|Purchase order associated with this invoice.|
|Supplier bank name|Bank name of the supplier.|
|Account number|Bank account number of the supplier.|
|ACH routing number|Unique, nine-digit number used to identify banks and financial institutions.|
|Swift code|Standard format for the Bank Identifier Code \(BIC\) that is used to identify banks and financial institutions.|
|Wire routing number|Unique, nine-digit number used to identify banks and financial institutions.|
|Tax rate|Tax rate applied on the invoice amount.|
|Amount invoiced|Total amount to be paid to the supplier including tax and shipping charges.|
|Subtotal|The total amount from all the invoice lines without tax and shipping charges.|
|Shipping amount|Shipping charges incurred for the invoice.|
|Other charges|Other charges applied on the invoice amount.|
|Tax amount|Tax applied on the invoice amount.|
|Invoice currency|The currency mentioned in the invoice.|
|Bill to company name|The name of the company to which the invoice is billed.|
|Bill to city|The city to which the invoice is sent.|
|Bill to country|The country to which the invoice is sent.|
|Bill to state/province|The state to which the invoice is sent.|
|Bill to street|The street address to which the invoice is sent.|
|Bill to zip/postal code|The zip code to which the invoice is sent.|
|Remit to city|The city to which the payment is made.|
|Remit to country|The country to which the payment is made.|
|Remit to state/province|The state to which the payment is made.|
|Remit to street|The street address to which the payment is made.|
|Remit to zip/postal code|The zip code to which this payment is made.|
|Invoice ship to city|The city to which the items on the purchase order should be shipped.|
|Invoice ship to country|The country to which the items on the purchase order should be shipped.|
|Invoice ship to state/province|The state to which the items on the purchase order should be shipped.|
|Invoice ship to street|The street address to which the items on the purchase order should be shipped.|
|Invoice ship to zip/postal code|The zip code to which the items on the purchase order should be shipped.|
|Invoice Line Fields|
|Line amount|Total amount for the invoice line item.|
|Line tax amount|Tax amount for the invoice line item.|
|Line unit price|Unit price of the line item in the invoice.|
|Line quantity|The number of items that have been invoiced.|
|Line description|Description for the invoice line.|

**Parent Topic:**[Invoice Processing use case](../concept/docintel-invoice-process-usecase.md)

**Related topics**  


[How Accounts Payable Operations integration with Document Intelligence works](../concept/apm-docintel-how-it-works.md)

[Configuring the invoice ingestion flows using Accounts Payable Operations integration with Document Intelligence](../concept/config-apo-docintel-integration.md)

