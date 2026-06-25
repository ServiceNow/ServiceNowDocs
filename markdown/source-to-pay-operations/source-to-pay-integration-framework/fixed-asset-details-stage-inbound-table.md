---
title: Fixed asset details stage inbound table
description: The Fixed asset details inbound \[sn\_fcms\_intg\_imp\_fixed\_asset\_details\] staging table temporarily stores important data about imported invoice line before this data is sent to the primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/fixed-asset-details-stage-inbound-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Inbound staging tables Sourcing Procurement, Inbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Fixed asset details stage inbound table

The Fixed asset details inbound \[sn\_fcms\_intg\_imp\_fixed\_asset\_details\] staging table temporarily stores important data about imported invoice line before this data is sent to the primary table.

## Fixed asset details inbound staging table

The following table lists the fields for the Fixed asset details inbound \[sn\_fcms\_intg\_imp\_fixed\_asset\_details\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|Asset id|String|Unique identifier for the fixed asset.|
|Asset number|String|Unique identifier generated within the ERP system for the fixed asset.|
|Capitalize on|String|Date on which the requester assumes the liability of the fixed asset, depending on the supplier incoterm.|
|Currency|String|Currency associated with the purchase of the fixed asset.|
|Depreciated amount|String|Amount that the fixed asset has depreciated by over time.|
|Depreciation life-cycle|String|Length of time in which the fixed asset is fully depreciated.|
|Depreciation start date|String|Start date of depreciation cycle.|
|Depreciation term|String|Frequency of depreciation throughout the life-cycle of the fixed asset.|
|ERP Asset number|String|Unique identifier generated within the ERP system for the fixed asset.|
|ERP Asset sub number|String|Unique identifier number that, when paired with the Asset number, identifies an asset.|
|ERP source|String|ERP source from which the fixed asset is imported.|
|Original value|String|Amount originally paid for the fixed asset.|
|Remaining value|String|Amount that the fixed asset is worth the current day, after factoring in depreciation.|
|Salvage value|String|Amount that the fixed asset is worth after it has come to the end of its life.|

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

