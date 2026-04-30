---
title: Fixed asset details stage inbound table
description: The Fixed asset details inbound \[sn\_fcms\_intg\_imp\_fixed\_asset\_details\] staging table temporarily stores important data about imported invoice line before this data is sent to the primary table.
locale: en-US
release: zurich
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Inbound staging tables for Sourcing and Procurement Operations, Inbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
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

**Parent Topic:**[Inbound staging tables for Sourcing and Procurement Operations](../concept/spo-inbound-staging-tables.md)

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

[GL Account Stage inbound staging table](spo-gl-account-inbound-table.md)

[Import Availability Updates inbound staging table](spo-import-avail-inbound-table.md)

[Availability Error staging table](availability-error-staging-table.md)

[Cost Allocation inbound staging table \(Deprecated\)](spo-cost-alloc-inbound-table.md)

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

