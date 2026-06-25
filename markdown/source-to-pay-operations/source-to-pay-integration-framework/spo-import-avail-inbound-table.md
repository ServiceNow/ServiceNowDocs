---
title: Import Availability Updates inbound staging table
description: The Import Availability Updates inbound \[sn\_spend\_intg\_imp\_availability\] staging table temporarily stores important data about cost allocations before this data is sent to the primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/spo-import-avail-inbound-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Inbound staging tables Sourcing Procurement, Inbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Import Availability Updates inbound staging table

The Import Availability Updates inbound \[sn\_spend\_intg\_imp\_availability\] staging table temporarily stores important data about cost allocations before this data is sent to the primary table.

The following table lists the mandatory and optional fields for the Import Availability Updates inbound \[sn\_spend\_intg\_imp\_availability\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|Available Units|String|Units that are available to be sold.|
|Customer ID|String|Unique identifier for each customer of the purchase order.|
|Catalog ID|String|Unique identifier for each catalog of the purchase order.|
|Supplier ID|String|Supplier ID for which the purchase order is generated.|
|Supplier part number|String|Supplier part number of the supplier product.|
|Third party import ID|String|Unique identifier for external data imports.|
|Unit|String|Unit or rate in which this product is sold by the supplier.|

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

[GL Account Stage inbound staging table]()

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

