---
title: Cost Allocation inbound staging table \(Deprecated\)
description: The Cost Allocation inbound \[sn\_spend\_intg\_imp\_cost\_allocation\] staging table temporarily stores important data about cost allocations before this data is sent to the primary table.
locale: en-US
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

[Invoice inbound staging table](spo-inbound-invoice-table.md)

[Purchase Order inbound staging table](spo-inbound-pur-order-table.md)

[Purchase Order Line inbound staging table](spo-inbound-pol-table.md)

[Receipt inbound staging table](spo-inbound-receipt-table.md)

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

