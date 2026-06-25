---
title: Cost Allocation inbound staging table \(Deprecated\)
description: The Cost Allocation inbound \[sn\_spend\_intg\_imp\_cost\_allocation\] staging table temporarily stores important data about cost allocations before this data is sent to the primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/spo-cost-alloc-inbound-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Inbound staging tables Sourcing Procurement, Inbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Cost Allocation inbound staging table \(Deprecated\)

The Cost Allocation inbound \[sn\_spend\_intg\_imp\_cost\_allocation\] staging table temporarily stores important data about cost allocations before this data is sent to the primary table.

**Important:** This table is deprecated; please use the new one in the ERP integration framework instead. For more information, see [KB2186786](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=0e382d13477966102c31b98a436d43fa).

The following table lists the fields for the Cost Allocation inbound \[sn\_spend\_intg\_imp\_cost\_allocation\] staging table.

<table id="table_c23_ss5_hzb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allocate by

</td><td>

String

</td><td>

Determines whether the cost allocation is based on amount or percentage.

</td></tr><tr><td>

Allocation amount

</td><td>

String

</td><td>

Amount that is allocated.

</td></tr><tr><td>

Allocation percentage

</td><td>

String

</td><td>

Percentage of cost allocation.

</td></tr><tr><td>

Cost center

</td><td>

String

</td><td>

Cost center associated with the cost allocation.

</td></tr><tr><td>

Cost owner

</td><td>

String

</td><td>

User who incurs the cost of the allocated transaction amount.

</td></tr><tr><td>

ERP CA number

</td><td>

String

</td><td>

CA number from the ERP system.

</td></tr><tr><td>

ERP line number

</td><td>

String

</td><td>

Purchase order line number from the ERP system.This is a mandatory field.

</td></tr><tr><td>

ERP PO number

</td><td>

String

</td><td>

Purchase order number from the ERP system.This is a mandatory field.

</td></tr><tr><td>

ERP source

</td><td>

String

</td><td>

ERP source from which data is imported. For purchase order, receipt, and invoice integrations, the ERP source is determined through the legal entity associated with these records.This is a mandatory field.

</td></tr><tr><td>

Order line

</td><td>

String

</td><td>

Order line associated with the cost allocation.

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

[Invoice inbound staging table]()

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

