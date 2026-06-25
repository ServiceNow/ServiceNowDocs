---
title: Legal Entity Stage inbound staging table
description: The Legal entity stage inbound \[sn\_fcms\_intg\_legal\_entity\_stage\] staging table temporarily stores important data about legal entities before this data is sent to the primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/spo-legal-entity-inbound-table.html
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

