---
title: Product Model Stage inbound staging table
description: The Product Model Stage inbound \[sn\_fcms\_intg\_cmdb\_model\_stage\] staging table temporarily stores important data about product models before this data is sent to the primary table.
locale: en-US
release: yokohama
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Inbound staging tables for Sourcing and Procurement Operations, Inbound staging tables for Source-to-Pay Operations, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Product Model Stage inbound staging table

The Product Model Stage inbound \[sn\_fcms\_intg\_cmdb\_model\_stage\] staging table temporarily stores important data about product models before this data is sent to the primary table.

The following table lists the mandatory fields for the Product Model Stage inbound \[sn\_fcms\_intg\_cmdb\_model\_stage\] staging table.

<table id="table_c23_ss5_hzb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Asset tracking

</td><td>

String

</td><td>

Process by which the model can be tracked.Select one of these options:-   Leave to Category: Model is transparent and the category defines the asset class.
-   Create Consumable Asset: Model forces the asset class to be consumable, regardless of what the category defines as the asset class.
-   Don't create assets: Model blocks asset instantiation, regardless of what the category defines as the asset class.

</td></tr><tr><td>

Description

</td><td>

String

</td><td>

Description of the product model for the buyer.

</td></tr><tr><td>

ERP source

</td><td>

String

</td><td>

ERP source from which data is imported. For purchase order, receipt, and invoice integrations, the ERP source is determined through the legal entity associated with these records.

</td></tr><tr><td>

Model category

</td><td>

String

</td><td>

Category to which the model belongs to.

</td></tr><tr><td>

Model number

</td><td>

String

</td><td>

Specific model number that is assigned to the item by the manufacturer.

</td></tr><tr><td>

Name

</td><td>

String

</td><td>

Name of the product model.

</td></tr><tr><td>

Product category

</td><td>

String

</td><td>

Category to which the product belongs to.

</td></tr><tr><td>

Short description

</td><td>

String

</td><td>

Brief description of the product model.

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

[Inbound Invoice staging table](spo-inbound-invoice-table.md)

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

