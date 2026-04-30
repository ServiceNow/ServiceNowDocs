---
title: Outbound invoice line staging table
description: The Outbound invoice line \[sn\_spend\_intg\_outbound\_invoice\_line\] staging table stores important invoice line data so that an ERP integrator can export this data to a third-party ERP system.
locale: en-US
release: xanadu
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Outbound staging tables for Accounts Payable Operations, Outbound staging tables for Source-to-Pay Operations, Source-to-Pay integration framework, Source-to-Pay integration with third-party applications, Source-to-Pay Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Outbound invoice line staging table

The Outbound invoice line \[sn\_spend\_intg\_outbound\_invoice\_line\] staging table stores important invoice line data so that an ERP integrator can export this data to a third-party ERP system.

## Outbound invoice line staging table

The following table lists both the mandatory and optional fields for the Outbound invoice line \[sn\_spend\_intg\_outbound\_invoice\_line\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|Cost center|Reference|Cost center for which the invoice is generated.|
|ERP line number|String|A unique identifier generated within an ERP system for the purchase order line.|
|ERP source|String|Target ERP where the invoice will be posted.|
|Final tax|String|Final tax on the invoice amount.|
|GL account|Reference|Account used to generate the invoice.|
|Integration status|String|Current status of the outbound invoice line integration process.|
|Invoice|Reference|Transaction record used to track purchase between shopper and supplier.|
|Invoice line status|String|Current status of this invoice line.|
|Line amount invoiced|String|Total amount for the invoice line.|
|Line description|String|Description of the line item in the invoice.|
|Line quantity|String|Number of items that have been invoiced.|
|Line unit price|String|Unit price of the line item in the invoice.|
|Number|String|An auto-generated number that uniquely identifies the invoice.|
|Processing message|String|A message that describes the current processing status.|
|Purchase order line|Reference|Purchase line related to this invoiced amount.|
|Ship to city|String|City to which the items on the purchase order should be shipped.|
|Ship to country|Reference|Country to which the items on the purchase order should be shipped.|
|Ship to state/province|String|State or province to which the items on the purchase order should be shipped.|
|Ship to street|String|Street address to which the items on the purchase order should be shipped.|
|Ship to zip/postal code|String|ZIP or postal code to which the items on the purchase order should be shipped.|
|Subtotal|String|Total amount of money to be paid to the supplier excluding tax and shipping charges.|
|Supplier part number|String|Supplier part number of the supplier product.|
|Tax amount|String|Tax rate applied on the invoice amount.|
|Tax code|Reference|Tax code of the invoice.|
|Tax code - deprecated|String|Indicates whether the Tax code on the invoice is deprecated or not.|
|Tax jurisdiction code|String|Tax code jurisdiction to which the tax must be paid.|
|Unit|Reference|Unit or rate in which this product is sold by the supplier.|

