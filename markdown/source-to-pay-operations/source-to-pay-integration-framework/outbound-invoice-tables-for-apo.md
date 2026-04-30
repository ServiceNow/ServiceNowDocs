---
title: Outbound invoice staging table
description: The outbound invoice \[sn\_spend\_intg\_outbound\_invoice\] staging table stores important data about invoices so that an ERP integrator can export this data to a third-party ERP system.
locale: en-US
release: xanadu
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Outbound staging tables for Accounts Payable Operations, Outbound staging tables for Source-to-Pay Operations, Source-to-Pay integration framework, Source-to-Pay integration with third-party applications, Source-to-Pay Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Outbound invoice staging table

The outbound invoice \[sn\_spend\_intg\_outbound\_invoice\] staging table stores important data about invoices so that an ERP integrator can export this data to a third-party ERP system.

## Outbound invoice staging table

The following table lists both the mandatory and optional fields for the outbound invoice \[sn\_spend\_intg\_outbound\_invoice\] staging table.

<table id="table_jf4_gyw_rbc"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Amount invoiced

</td><td>

String

</td><td>

Total amount for the invoice.

</td></tr><tr><td>

Business owner

</td><td>

String

</td><td>

An individual or group who owns the invoice.

</td></tr><tr><td>

Currency

</td><td>

String

</td><td>

Currency format associated with the invoice.

</td></tr><tr><td>

Default tax code

</td><td>

Reference

</td><td>

Default tax code levied on the total invoice amount.

</td></tr><tr><td>

Default tax code - deprecated

</td><td>

String

</td><td>

Indicates whether the Tax code on the invoice is deprecated or not.

</td></tr><tr><td>

Default tax jurisdiction code

</td><td>

String

</td><td>

Tax code jurisdiction to which the tax must be paid.

</td></tr><tr><td>

Discounts

</td><td>

String

</td><td>

Discounts applied on the invoice amount.

</td></tr><tr><td>

ERP number

</td><td>

String

</td><td>

Unique number generated within the ERP system for the purchase order.

</td></tr><tr><td>

ERP posting date

</td><td>

String

</td><td>

Date on which the invoice is posted in the ERP system.

</td></tr><tr><td>

ERP source

</td><td>

String

</td><td>

Target ERP where the invoice will be posted.

</td></tr><tr><td>

Final tax

</td><td>

String

</td><td>

Final tax on the invoice amount.

</td></tr><tr><td>

Integration status

</td><td>

String

</td><td>

Current status of the outbound invoice integration process.

</td></tr><tr><td>

Invoice date

</td><td>

String

</td><td>

Date on which this invoice is created.

</td></tr><tr><td>

Invoice status

</td><td>

String

</td><td>

Current status of this invoice.

</td></tr><tr><td>

Invoice type

</td><td>

String

</td><td>

Type of invoice for processing.**Note:** Accounts Payable Operations supports invoices of type **PO invoice** and **Non-PO invoice**.

</td></tr><tr><td>

Legal entity

</td><td>

Reference

</td><td>

Internal legal entity which incurs the cost of this invoice.

</td></tr><tr><td>

Number

</td><td>

String

</td><td>

An auto-generated number that uniquely identifies the invoice.

</td></tr><tr><td>

Original invoice

</td><td>

String

</td><td>

A unique invoice number created by the Supplier.

</td></tr><tr><td>

Other charges

</td><td>

String

</td><td>

Other charges applied on the invoice amount.

</td></tr><tr><td>

Payment terms

</td><td>

Reference

</td><td>

How and when to make payment for the products and services.

</td></tr><tr><td>

Processing message

</td><td>

String

</td><td>

A message that describes the current processing status.

</td></tr><tr><td>

Purchase order

</td><td>

Reference

</td><td>

Purchase order associated with this invoice.

</td></tr><tr><td>

Remit to city

</td><td>

String

</td><td>

City to which the payment is made.

</td></tr><tr><td>

Remit to country

</td><td>

Reference

</td><td>

Country to which the payment is made.

</td></tr><tr><td>

Remit to state/province

</td><td>

String

</td><td>

State or province to which the payment is made.

</td></tr><tr><td>

Remit to street

</td><td>

String

</td><td>

Street address to which the payment is made.

</td></tr><tr><td>

Remit to zip/postal code

</td><td>

String

</td><td>

ZIP or postal code to which the payment is made.

</td></tr><tr><td>

Ship from city

</td><td>

String

</td><td>

City from which the items on the purchase order is shipped.

</td></tr><tr><td>

Ship from country

</td><td>

Reference

</td><td>

Country from which the items on the purchase order is shipped.

</td></tr><tr><td>

Ship from state/province

</td><td>

String

</td><td>

State or province from which the items on the purchase order is shipped.

</td></tr><tr><td>

Ship from street

</td><td>

String

</td><td>

Street address from which the items on the purchase order is shipped.

</td></tr><tr><td>

Ship from zip/postal code

</td><td>

String

</td><td>

ZIP or postal code from which the items on the purchase order is shipped.

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

State or province to which the items on the purchase order should be shipped.

</td></tr><tr><td>

Ship to street

</td><td>

String

</td><td>

Street address to which the items on the purchase order should be shipped.

</td></tr><tr><td>

Ship to zip/postal code

</td><td>

String

</td><td>

ZIP or postal code to which the items on the purchase order should be shipped.

</td></tr><tr><td>

Shipping amount

</td><td>

String

</td><td>

Shipping charges incurred for the invoice.

</td></tr><tr><td>

Subtotal

</td><td>

String

</td><td>

Total amount of money to be paid to the supplier excluding tax and shipping charges.

</td></tr><tr><td>

Supplier

</td><td>

Reference

</td><td>

Supplier who delivers the product or service.

</td></tr><tr><td>

Supplier invoice number

</td><td>

String

</td><td>

Invoice number of the supplier invoice.

</td></tr><tr><td>

Tax amount

</td><td>

String

</td><td>

Tax rate applied on the invoice amount.

</td></tr></tbody>
</table>