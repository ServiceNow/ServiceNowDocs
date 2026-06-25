---
title: Cost Center Stage inbound staging table
description: The Cost Center Stage inbound \[sn\_fcms\_intg\_imp\_cost\_center\] staging table temporarily stores important data about cost centers before this data is sent to the primary table. You can use this table to lookup all the cost center details.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/spo-cost-center-inbound-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Inbound staging tables Sourcing Procurement, Inbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Cost Center Stage inbound staging table

The Cost Center Stage inbound \[sn\_fcms\_intg\_imp\_cost\_center\] staging table temporarily stores important data about cost centers before this data is sent to the primary table. You can use this table to lookup all the cost center details.

The following table lists the mandatory fields for the Cost Center Stage inbound \[sn\_fcms\_intg\_imp\_cost\_center\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|Account number|String|Account number of the cost center|
|Available for user|String|Users that are applicable to the cost center|
|Code|String|Code of the cost center|
|Cost center type|String|Type of cost center|
|Controlling area|String|Controlling area of the cost center|
|ERP source|String|ERP source from which data is imported. For purchase order, receipt, and invoice integrations, the ERP source is determined through the legal entity associated with these records.|
|Legal entity|String|Detailed information about individual suppliers, including banking details, payment methods, and credit terms.|
|Manager|String|Name of the manager of the cost center|
|Name|String|Name of the cost center|
|Profit center|String|Profit centers within the organization, enabling financial reporting and analysis by business units or operational segments.|
|Valid from|String|Date the cost center is valid from|
|Valid to|String|Date the cost center is valid to|

**Parent Topic:**[Inbound staging tables for Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-inbound-staging-tables.md)

**Related topics**  


[CMDB Model Category Stage inbound staging table]()

[CMDB Service Model Stage inbound staging table]()

[CMN Location Stage inbound staging table]()

[Catalog Import staging table]()

[Catalog Error staging table]()

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

