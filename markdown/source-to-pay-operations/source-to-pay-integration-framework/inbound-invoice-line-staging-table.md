---
title: Invoice line import inbound staging table
description: The Invoice line import inbound \[sn\_spend\_intg\_imp\_invoice\_line\] staging table temporarily stores important data about imported invoice line before this data is sent to the \[sn\_shop\_invoice\_line\] primary table.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Inbound staging tables for Accounts Payable Operations, Inbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Invoice line import inbound staging table

The Invoice line import inbound \[sn\_spend\_intg\_imp\_invoice\_line\] staging table temporarily stores important data about imported invoice line before this data is sent to the \[sn\_shop\_invoice\_line\] primary table.

## Invoice line import inbound staging table

The following table lists the mandatory fields for the Invoice line import inbound \[sn\_spend\_intg\_imp\_invoice\_line\] staging table.

<table id="table_imh_yxw_rbc"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cost center

</td><td>

String

</td><td>

Cost center for which the invoice is generated.

</td></tr><tr><td>

Currency

</td><td>

String

</td><td>

Currency format associated with the invoice.

</td></tr><tr><td>

ERP line number

</td><td>

String

</td><td>

ERP line number.

</td></tr><tr><td>

ERP source

</td><td>

String

</td><td>

Available ERP source.This is a mandatory field.

</td></tr><tr><td>

External invoice number

</td><td>

String

</td><td>

Invoice number from external invoice.

</td></tr><tr><td>

External invoice source

</td><td>

String

</td><td>

Name of the third party application associated with the invoice. Derive logic from external invoice number.This is a mandatory field.

</td></tr><tr><td>

Final tax

</td><td>

String

</td><td>

Final tax.

</td></tr><tr><td>

GL account

</td><td>

String

</td><td>

Account used to generate the invoice.

</td></tr><tr><td>

Inbound source

</td><td>

String

</td><td>

External invoice source.

</td></tr><tr><td>

Line amount invoiced

</td><td>

String

</td><td>

The total cost which is being billed for this good or service.

</td></tr><tr><td>

Line description

</td><td>

String

</td><td>

Description of the invoice line.This is a mandatory field.

</td></tr><tr><td>

Line quantity

</td><td>

Decimal number

</td><td>

Number of items that have been invoiced.This is a mandatory field.

</td></tr><tr><td>

Line unit price

</td><td>

Decimal number

</td><td>

Unit price of the line item in the invoice.This is a mandatory field.

</td></tr><tr><td>

Purchase order line

</td><td>

String

</td><td>

Purchase line related to the invoiced amount.

</td></tr><tr><td>

Ship to city

</td><td>

String

</td><td>

City to which the items on the purchase order should be shipped.

</td></tr><tr><td>

Ship to country

</td><td>

String

</td><td>

Country to which the items on the purchase order should be shipped.

</td></tr><tr><td>

Ship to state/province

</td><td>

String

</td><td>

State to which the items on the purchase order should be shipped.

</td></tr><tr><td>

Ship to street

</td><td>

String

</td><td>

Address to which the items on the purchase order should be shipped.

</td></tr><tr><td>

Ship to zip/postal code

</td><td>

String

</td><td>

Zip code to which the items on the purchase order should be shipped.

</td></tr><tr><td>

Status

</td><td>

String

</td><td>

Current status of this invoice line.

</td></tr><tr><td>

Subtotal

</td><td>

Decimal number Example \(12345.65\)

</td><td>

Total amount of money to be paid to the supplier excluding tax and shipping charges.This is a mandatory field.

</td></tr><tr><td>

Supplier part number

</td><td>

String

</td><td>

Supplier part number of the supplier product.

</td></tr><tr><td>

Supplier tax rate

</td><td>

String

</td><td>

Supplier tax rate.

</td></tr><tr><td>

Target ERP

</td><td>

String

</td><td>

ERP number of inbound source.

</td></tr><tr><td>

Tax amount

</td><td>

String

</td><td>

Tax for the invoice amount.

</td></tr><tr><td>

Tax code

</td><td>

String

</td><td>

Tax code of the invoice.

</td></tr><tr><td>

Third party import ID

</td><td>

String

</td><td>

Unique identifier for external data imports.

</td></tr><tr><td>

Unit

</td><td>

String

</td><td>

The unit or rate in which this product is sold by the supplier.

</td></tr></tbody>
</table>**Parent Topic:**[Inbound staging tables for Accounts Payable Operations](../../accounts-payable-operations/concept/inbound-staging-tables-for-apo.md)

**Related topics**  


[Invoice import inbound staging table](inbound-invoice-import-staging-table.md)

[Import error staging table](../../accounts-payable-operations/reference/import-error-staging-table.md)

[Invoice payment detail import inbound table](../../accounts-payable-operations/reference/invoice-payment-detail-staging-table.md)

[Organization tax details inbound staging table](../../supplier-lifecycle-operations/reference/slo-org-tax-details-inbound-table.md)

[Invoice tax line staging table](../../source-to-pay-operations/reference/inbound-invoice-tax-line-staging-table-apo.md)

[Invoice staging table](../../accounts-payable-operations/reference/invoice-staging-table.md)

[Invoice line stage table](../../accounts-payable-operations/reference/invoice-line-staging-table.md)

