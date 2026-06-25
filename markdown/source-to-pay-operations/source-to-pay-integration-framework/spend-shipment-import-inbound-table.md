---
title: Spend Shipment Import inbound staging table
description: The Spend Shipment Import inbound \[sn\_spend\_intg\_imp\_shipment\] staging table temporarily stores important data about spend shipment imports before this data is sent to the primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/spend-shipment-import-inbound-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Inbound staging tables Sourcing Procurement, Inbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Spend Shipment Import inbound staging table

The Spend Shipment Import inbound \[sn\_spend\_intg\_imp\_shipment\] staging table temporarily stores important data about spend shipment imports before this data is sent to the primary table.

The following table lists both the mandatory and optional fields for the Spend Shipment Import inbound \[sn\_spend\_intg\_imp\_shipment\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|Actual shipment date|String|Date at which the product was shipped.|
|City|String|Name of the city of the shipment.|
|Country|String|Name of the country of the shipment.|
|Customer ID|String|Unique identifier for each customer of the shipment.|
|Estimated shipment date|String|Date at which the product is estimated to be shipped.|
|Line number|String|Line number of the shipment.|
|Name|String|Name of the shipment.|
|Order number|String|Unique order number of the shipment.|
|Planned shipment date|String|Date at which the product is planned to be shipped.|
|Product details|String|Details of the product to be shipped.|
|Punchout|String|Punch out details of the shipment.|
|Sales order line number|String|Sales order line number of the shipment.|
|Sales order number|String|Sales order number associated with the shipment.|
|Ship to|String|Shipping location of the product.|
|Shipment Import|String|Number of shipments to be imported.|
|Shipment quantity|String|Number of shipments to be shipped.|
|Shipment type|String|Type of shipment.|
|Shipping carrier|String|Name of the shipping carrier.|
|State|String|Name of the state of the shipment.|
|Street|String|Street of the shipment.|
|Supplier ID|String|ID of the supplier.|
|Supplier shipment number|String|Shipment number of the supplier.|
|Third party import ID|String|Third party import ID of the shipment.|
|Tracking number|String|Tracking number of the shipment.|
|Zip code|String|ZIP code of the shipment.|

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

[Shipment Error staging table]()

[Supplier Product Stage inbound staging table]()

[Third Party Sourcing Registration staging table]()

[Third Party Unit Mapping staging table]()

[Third Party Unit staging table]()

[Unit of Measure inbound staging table]()

