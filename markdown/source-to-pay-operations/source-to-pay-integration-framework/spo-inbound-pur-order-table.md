---
title: Purchase Order inbound staging table
description: The Purchase Order inbound \[sn\_fcms\_intg\_imp\_order\] staging table temporarily stores important data about purchase orders before this data is sent to the primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/spo-inbound-pur-order-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Inbound staging tables Sourcing Procurement, Inbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Purchase Order inbound staging table

The Purchase Order inbound \[sn\_fcms\_intg\_imp\_order\] staging table temporarily stores important data about purchase orders before this data is sent to the primary table.

The following table lists fields for the Purchase Order inbound \[sn\_fcms\_intg\_imp\_order\] staging table.

<table id="table_c23_ss5_hzb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Blanket order end date

</td><td>

String

</td><td>

Date on which the blanket order is expected to end.If you're unsure of the delivery date of the product, you can provide an estimated time frame, which then creates a blanket order.

</td></tr><tr><td>

Blanket order start date

</td><td>

String

</td><td>

Date on which the blanket order is expected to start.If you're unsure of the delivery date of the product, you can provide an estimated time frame, which then creates a blanket order.

</td></tr><tr><td>

Business owner

</td><td>

String

</td><td>

The user who placed the order.

</td></tr><tr><td>

Cost center

</td><td>

String

</td><td>

Cost center that incurs the expense of the order.

</td></tr><tr><td>

ERP PO number

</td><td>

String

</td><td>

Purchase order number from the ERP system. This is a mandatory field.

</td></tr><tr><td>

ERP source

</td><td>

String

</td><td>

ERP source from which data is imported. For purchase order, receipt, and invoice integrations, the ERP source is determined through the legal entity associated with these records.This is a mandatory field.

</td></tr><tr><td>

Legal entity

</td><td>

String

</td><td>

Legal entity corresponding to a purchase.

</td></tr><tr><td>

Order type

</td><td>

String

</td><td>

Type of the purchase order- Standard or Blanket.

</td></tr><tr><td>

Payment term

</td><td>

String

</td><td>

The agreed upon time and conditions under which a payment to a supplier is made.

</td></tr><tr><td>

PO amount

</td><td>

String

</td><td>

Total amount of the purchase order.

</td></tr><tr><td>

PO amount currency

</td><td>

String

</td><td>

Currency of the purchase order.

</td></tr><tr><td>

PO status

</td><td>

String

</td><td>

Status of the purchase order.

</td></tr><tr><td>

Purchasing organization

</td><td>

String

</td><td>

The organization making the purchase order.

</td></tr><tr><td>

Supplier company name

</td><td>

String

</td><td>

Supplier company name for which the purchase order is generated.

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

[Invoice inbound staging table]()

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

