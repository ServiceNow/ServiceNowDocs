---
title: Product Model Stage inbound staging table
description: The Product Model Stage inbound \[sn\_fcms\_intg\_cmdb\_model\_stage\] staging table temporarily stores important data about product models before this data is sent to the primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/spo-prod-mod-inbound-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Inbound staging tables Sourcing Procurement, Inbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
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

