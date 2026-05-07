---
title: Legal Entity Stage inbound staging table
description: The Legal entity stage inbound \[sn\_fcms\_intg\_legal\_entity\_stage\] staging table temporarily stores important data about legal entities before this data is sent to the primary table.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Inbound staging tables Sourcing Procurement, Inbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Legal Entity Stage inbound staging table

The Legal entity stage inbound \[sn\_fcms\_intg\_legal\_entity\_stage\] staging table temporarily stores important data about legal entities before this data is sent to the primary table.

The following table lists the fields for the Legal Entity Stage inbound \[sn\_fcms\_intg\_legal\_entity\_stage\] staging table.

<table id="table_c23_ss5_hzb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

City

</td><td>

String

</td><td>

City where the legal entity is located.

</td></tr><tr><td>

Country

</td><td>

String

</td><td>

Country where the legal entity is located.

</td></tr><tr><td>

ERP company code

</td><td>

String

</td><td>

Company code of the supplier in the ERP system.This is a mandatory field.

</td></tr><tr><td>

ERP source

</td><td>

String

</td><td>

ERP source from which data is imported. For purchase order, receipt, and invoice integrations, the ERP source is determined through the legal entity associated with these records.This is a mandatory field.

</td></tr><tr><td>

Global company

</td><td>

String

</td><td>

Global company that the entity is linked to.

</td></tr><tr><td>

Industry

</td><td>

String

</td><td>

Industry type of the legal entity.

</td></tr><tr><td>

Legal name

</td><td>

String

</td><td>

Legal name of the entity that corresponds to its operating location.

</td></tr><tr><td>

Local currency

</td><td>

String

</td><td>

Local currency that corresponds to the entity's operating location.

</td></tr><tr><td>

Street

</td><td>

String

</td><td>

Street where the legal entity is located.

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

[Cost Allocation inbound staging table \(Deprecated\)](spo-cost-alloc-inbound-table.md)

[Invoice inbound staging table](spo-inbound-invoice-table.md)

[Purchase Order inbound staging table](spo-inbound-pur-order-table.md)

[Purchase Order Line inbound staging table](spo-inbound-pol-table.md)

[Receipt inbound staging table](spo-inbound-receipt-table.md)

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

