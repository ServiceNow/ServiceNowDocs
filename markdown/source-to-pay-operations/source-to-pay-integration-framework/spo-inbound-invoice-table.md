---
title: Invoice inbound staging table
description: The Invoice inbound \[sn\_shop\_invoice\] staging table temporarily stores important data about shopping invoices before this data is sent to the primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/spo-inbound-invoice-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Inbound staging tables Sourcing Procurement, Inbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Invoice inbound staging table

The Invoice inbound \[sn\_shop\_invoice\] staging table temporarily stores important data about shopping invoices before this data is sent to the primary table.

## Invoice inboumd staging table

The following table lists fields for Invoice inbound \[sn\_shop\_invoice\] staging table.

<table id="table_nl4_txw_rbc"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

External invoice number

</td><td>

String

</td><td>

Invoice number originated from a third party application. This is a mandatory field.

</td></tr><tr><td>

Inbound source

</td><td>

String

</td><td>

Individual or group who owns the invoice.

</td></tr><tr><td>

Currency

</td><td>

String

</td><td>

Currency format associated with this invoice.

</td></tr><tr><td>

Discounts

</td><td>

String

</td><td>

Discounts applied on the invoice.

</td></tr><tr><td>

ERP number

</td><td>

String

</td><td>

Unique number generated within the ERP system for the purchase order.

</td></tr><tr><td>

ERP source

</td><td>

String

</td><td>

The available ERP.This is a mandatory field.

</td></tr><tr><td>

External invoice number

</td><td>

String

</td><td>

Invoice number originated from a third party application. This is a mandatory field.

</td></tr><tr><td>

External invoice source

</td><td>

String

</td><td>

Name of the third party application associated with the invoice.This is a mandatory field.

</td></tr><tr><td>

Final tax

</td><td>

String

</td><td>

Total amount of tax to be paid.

</td></tr><tr><td>

Inbound source

</td><td>

String

</td><td>

External source system from where the invoice is received.

</td></tr><tr><td>

Invoice date

</td><td>

String \(yyyy-mm-dd\)

</td><td>

Date on which the invoice is created.This is a mandatory field.

</td></tr><tr><td>

Invoice date

</td><td>

String

</td><td>

Date on which the invoice was created.

</td></tr><tr><td>

Invoice line count

</td><td>

String

</td><td>

Total number of invoice lines in an invoice.

</td></tr><tr><td>

Invoice type

</td><td>

String

</td><td>

Type of the invoice for processing.

</td></tr><tr><td>

Legal entity

</td><td>

String

</td><td>

Name of the legal entity of the supplier.

</td></tr><tr><td>

Original invoice

</td><td>

String

</td><td>

Unique invoice number created by the Supplier.

</td></tr><tr><td>

Other charges

</td><td>

String

</td><td>

Other additional charges associated with the invoice.This is a mandatory field.

</td></tr><tr><td>

Payment terms

</td><td>

String

</td><td>

The agreed upon time and conditions under which a payment to a supplier is made.

</td></tr><tr><td>

Purchase order

</td><td>

String

</td><td>

The purchase order against which the invoice is created.

</td></tr><tr><td>

Remit to city

</td><td>

String

</td><td>

City to which the payment is made.

</td></tr><tr><td>

Remit to country

</td><td>

String

</td><td>

Country to which the payment is made.

</td></tr><tr><td>

Remit to state/province

</td><td>

String

</td><td>

State to which the payment is made.

</td></tr><tr><td>

Remit to street

</td><td>

String

</td><td>

Street to which the payment is made.

</td></tr><tr><td>

Remit to zip/postal code

</td><td>

String

</td><td>

Zip code to which the payment is made.

</td></tr><tr><td>

Ship from city

</td><td>

String

</td><td>

City from which the items on the purchase order are shipped.

</td></tr><tr><td>

Ship from country

</td><td>

String

</td><td>

Country from which the items on the purchase order are shipped.

</td></tr><tr><td>

Ship from state/province

</td><td>

String

</td><td>

State from which the items on the purchase order are shipped.

</td></tr><tr><td>

Ship from street

</td><td>

String

</td><td>

Street from which the items on the purchase order are shipped.

</td></tr><tr><td>

Ship from zip/postal code

</td><td>

String

</td><td>

Zip code from which the items on the purchase order are shipped.

</td></tr><tr><td>

Shipping amount

</td><td>

String

</td><td>

Shipping charges incurred for the invoice.

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

Street to which the items on the purchase order should be shipped.

</td></tr><tr><td>

Ship to zip/postal code

</td><td>

String

</td><td>

Zip code to which the items on the purchase order is shipped.

</td></tr><tr><td>

Status

</td><td>

String

</td><td>

Current status of the inbound invoice.

</td></tr><tr><td>

Subtotal

</td><td>

String

</td><td>

Total amount of money to be paid to the supplier excluding tax and shipping charges.This is a mandatory field.

</td></tr><tr><td>

Supplier

</td><td>

String

</td><td>

Name of the supplier from whom the good or service is procured.This is a mandatory field.

</td></tr><tr><td>

Supplier invoice number

</td><td>

String

</td><td>

Unique invoice number created by the Supplier.

</td></tr><tr><td>

Supplier tax id

</td><td>

String

</td><td>

Tax ID associated to the third party reseller.

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

Target ERP where the invoice is posted.

</td></tr><tr><td>

Tax amount

</td><td>

String

</td><td>

Tax amount levied on the total invoice amount.

</td></tr><tr><td>

Third party import ID

</td><td>

String

</td><td>

A unique identifier for external data imports.

</td></tr></tbody>
</table>**Parent Topic:**[Inbound staging tables for Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-inbound-staging-tables.md)

**Related topics**  


[CMDB Model Category Stage inbound staging table]()

[CMDB Service Model Stage inbound staging table]()

[CMN Location Stage inbound staging table]()

[Catalog Import staging table]()

[Catalog Error staging table]()

[Cost Center Stage inbound staging table]()

[Department Stage inbound staging table]()

[ERP Plant Address Mapping Stage inbound staging table]()

[FX Currency Stage inbound staging table]()

[FX Rate Stage inbound staging table]()

[Fixed asset details stage inbound table]()

[GL Account Stage inbound staging table]()

[Import Availability Updates inbound staging table]()

[Availability Error staging table]()

[Cost Allocation inbound staging table \(Deprecated\)]()

[Purchase Order inbound staging table]()

[Purchase Order Line inbound staging table]()

[Receipt inbound staging table]()

[Legal Entity Stage inbound staging table]()

[Office Location Stage inbound staging table]()

[Order Acknowledgement staging table]()

[Order Acknowledgement Error staging table]()

[Payment Terms Stage inbound staging table]()

[Price Import staging table]()

[Price Error outbound staging table]()

[Product Model Stage inbound staging table]()

[Purchase Entity Stage inbound staging table]()

[Purchase Line Stage inbound staging table]()

[Purchase Requisition staging table]()

[Spend Shipment Import inbound staging table]()

[Shipment Error staging table]()

[Supplier Product Stage inbound staging table]()

[Third Party Sourcing Registration staging table]()

[Third Party Unit Mapping staging table]()

[Third Party Unit staging table]()

[Unit of Measure inbound staging table]()

