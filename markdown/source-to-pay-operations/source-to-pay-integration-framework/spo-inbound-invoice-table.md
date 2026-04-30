---
title: Inbound Invoice staging table
description: The Inbound Invoice \[sn\_shop\_invoice\] staging table temporarily stores important data about shopping invoices before this data is sent to the primary table.
locale: en-US
release: yokohama
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Inbound staging tables for Sourcing and Procurement Operations, Inbound staging tables for Source-to-Pay Operations, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Inbound Invoice staging table

The Inbound Invoice \[sn\_shop\_invoice\] staging table temporarily stores important data about shopping invoices before this data is sent to the primary table.

## Inbound Invoice staging table

The following table lists fields for Inbound Invoice \[sn\_shop\_invoice\] staging table.

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
</table>**Parent Topic:**[Inbound staging tables for Sourcing and Procurement Operations](../concept/spo-inbound-staging-tables.md)

**Related topics**  


[CMDB Model Category Stage inbound staging table](spo-prod-cate-inbound-table.md)

[CMDB Service Model Stage inbound staging table](spo-serv-mod-inbound-table.md)

[CMN Location Stage inbound staging table](spo-loc-inbound-table.md)

[Catalog Import staging table](catalog-import-staging-table.md)

[Catalog Error staging table](catalog-error.md)

[Cost Center Stage inbound staging table](spo-cost-center-inbound-table.md)

[Department Stage inbound staging table](spo-dept-inbound-table.md)

[ERP Plant Address Mapping Stage inbound staging table](spo-erp-plant-address-inbound-table.md)

[FX Currency Stage inbound staging table](spo-fx-currency-inbound-table.md)

[FX Rate Stage inbound staging table](spo-fx-rate-inbound-table.md)

[Fixed asset details stage inbound table](fixed-asset-details-stage-inbound-table.md)

[GL Account Stage inbound staging table](spo-gl-account-inbound-table.md)

[Import Availability Updates inbound staging table](spo-import-avail-inbound-table.md)

[Availability Error staging table](availability-error-staging-table.md)

[Inbound Cost Allocation staging table](spo-cost-alloc-inbound-table.md)

[Inbound Purchase Order staging table](spo-inbound-pur-order-table.md)

[Inbound Purchase Order Line staging table](spo-inbound-pol-table.md)

[Inbound Receipt staging table](spo-inbound-receipt-table.md)

[Legal Entity Stage inbound staging table](spo-legal-entity-inbound-table.md)

[Office Location Stage inbound staging table](spo-office-loc-inbound-table.md)

[Order Acknowledgement staging table](order-acknowledgement-staging-table.md)

[Order Acknowledgement Error staging table](order-acknowledgement-error.md)

[Payment Terms Stage inbound staging table](spo-pay-terms-inbound-table.md)

[Price Import staging table](price-import-staging-table.md)

[Price Error outbound staging table](price-error-staging-table.md)

[Product Model Stage inbound staging table](spo-prod-mod-inbound-table.md)

[Purchase Entity Stage inbound staging table](spo-purch-entity-inbound-table.md)

[Purchase Line Stage inbound staging table](spo-purch-line-stage-inbound-table.md)

[Purchase Requisition staging table](purchase-requisition-staging-table.md)

[Spend Shipment Import inbound staging table](spend-shipment-import-inbound-table.md)

[Shipment Error staging table](shipment-error-staging-table.md)

[Supplier Product Stage inbound staging table](spo-supp-prod-inbound-table.md)

[Third Party Sourcing Registration staging table](third-party-sourcing-registration-staging-table.md)

[Third Party Unit Mapping staging table](third-party-unit-mapping-staging-table.md)

[Third Party Unit staging table](third-party-unit-staging-table.md)

[Unit of Measure inbound staging table](unit-measure-inbound-staging-table.md)

