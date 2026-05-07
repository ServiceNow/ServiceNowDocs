---
title: Invoice staging table
description: The invoice staging \[sn\_ap\_ic\_invoice\_stage\] table temporarily stores the header-level invoice data from Document Intelligence before it is transferred to the invoice record.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-05-06"
reading_time_minutes: 3
breadcrumb: [Inbound staging tables for Accounts Payable Operations, Inbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Invoice staging table

The invoice staging \[sn\_ap\_ic\_invoice\_stage\] table temporarily stores the header-level invoice data from Document Intelligence before it is transferred to the invoice record.

## Invoice inbound staging table \(sn\_ap\_ic\_invoice\_stage\)

The following table lists the fields for the invoice inbound \[sn\_ap\_ic\_invoice\_stage\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|Number|string|Auto-generated identifier for the staging record. Read only.|
|Supplier invoice number|string|Invoice number as printed on the source document.|
|Supplier|string|Supplier name extracted from the document.|
|Supplier tax id|string|Supplier VAT or tax identification number.|
|Invoice date|string|Invoice date as extracted from the document \(raw string\).|
|Invoice date \(parsed\)|glide\_date|Parsed date field populated by Document Intelligence from the raw invoice date string.|
|Purchase order|string|PO number referenced on the invoice.|
|Subtotal|string|Invoice subtotal before tax and other charges.|
|Amount invoiced \(Transaction currency\)|string|Total invoiced amount in the transaction currency.|
|Tax rate|string|Tax rate as extracted from the document.|
|Tax amount|string|Tax amount as extracted from the document.|
|Shipping amount|string|Shipping charges extracted from the document.|
|Other charges|string|Miscellaneous charges extracted from the document.|
|Invoice currency|string|Currency code of the invoice.|
|Original invoice number|string|For credit memos, the number of the invoice being credited.|
|Bill to company name|string|Company name from the bill-to address on the invoice.|
|Bill to street|string|Street address from the bill-to address on the invoice.|
|Bill to city|string|City from the bill-to address on the invoice.|
|Bill to state/province|string|State or province from the bill-to address on the invoice.|
|Bill to country|string|Country from the bill-to address on the invoice.|
|Bill to zip/postal code|string|ZIP or postal code from the bill-to address on the invoice.|
|Remit to street|string|Street address for supplier payment remittance.|
|Remit to city|string|City for supplier payment remittance.|
|Remit to state/province|string|State or province for supplier payment remittance.|
|Remit to country|string|Country for supplier payment remittance.|
|Remit to zip/postal code|string|ZIP or postal code for supplier payment remittance.|
|Ship to street|string|Street address from the ship-to address on the invoice.|
|Ship to city|string|City from the ship-to address on the invoice.|
|Ship to state/province|string|State or province from the ship-to address on the invoice.|
|Ship to country|string|Country from the ship-to address on the invoice.|
|Ship to zip/postal code|string|ZIP or postal code from the ship-to address on the invoice.|
|Supplier bank name|string|Supplier bank name extracted for payment routing.|
|ACH routing number|string|ACH routing number extracted for payment routing.|
|Wire routing number|string|Wire transfer routing number extracted for payment routing.|
|Account number|string|Supplier bank account number extracted for payment routing.|
|Swift code|string|SWIFT code for international wire transfers.|
|Status|choice|Processing status of the staging record.|
|Invoice email|reference|Reference to the inbound email record that delivered this invoice.|
|Sender email address|string|Email address from which the invoice was sent.|
|Recipient email address|string|Email address that will receive the invoice.|
|Related invoice|reference|Reference to the invoice record created from this staging record.|

**Parent Topic:**[Inbound staging tables for Accounts Payable Operations](../concept/inbound-staging-tables-for-apo.md)

**Related topics**  


[Invoice import inbound staging table](../../source-to-pay-integrations/reference/inbound-invoice-import-staging-table.md)

[Import error staging table](import-error-staging-table.md)

[Invoice line import inbound staging table](../../source-to-pay-integrations/reference/inbound-invoice-line-staging-table.md)

[Invoice payment detail import inbound table](invoice-payment-detail-staging-table.md)

[Organization tax details inbound staging table](../../source-to-pay-integrations/reference/slo-org-tax-details-inbound-table.md)

[Invoice tax line staging table](../../source-to-pay-operations/reference/inbound-invoice-tax-line-staging-table-apo.md)

[Invoice line stage table](invoice-line-staging-table.md)

