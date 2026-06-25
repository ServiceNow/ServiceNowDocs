---
title: GL Account Stage inbound staging table
description: The GL Account Stage inbound \[sn\_fcms\_intg\_gl\_account\_stage\] staging table temporarily stores important data about General Ledger \(GL\) accounts before this data is sent to the primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/spo-gl-account-inbound-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Inbound staging tables Sourcing Procurement, Inbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# GL Account Stage inbound staging table

The GL Account Stage inbound \[sn\_fcms\_intg\_gl\_account\_stage\] staging table temporarily stores important data about General Ledger \(GL\) accounts before this data is sent to the primary table.

The following table lists the mandatory fields for the GL Account Stage inbound \[sn\_fcms\_intg\_gl\_account\_stage\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|Account currency|String|Currency name of the GL account.|
|Account name|String|Name of the GL account.|
|Alternate currency|String|Alternate currency name of the GL account.|
|Category|String|Category of the GL account.|
|Entity|String|Name of the entity.|
|ERP source|String|ERP source from which data is imported. For purchase order, receipt, and invoice integrations, the ERP source is determined through the legal entity associated with these records.|
|GL Account|String|Name of the general ledger account.|
|Inactive|String|Status of the GL account. By default the checkbox is inactive.|
|Ledger type|String|Type of ledger account.|
|Local currency|String|Local currency that corresponds to the entity's operating location.|
|Number|String|General ledger account number.|
|Short description|String|Description of the GL account.|
|Sub-ledger account|String|Sub-ledger account number.|
|Type|String|Type of GL account.|

**Parent Topic:**[Inbound staging tables for Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-inbound-staging-tables.md)

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

