---
title: Catalog Import staging table
description: The Catalog Import \[sn\_spend\_intg\_imp\_catalog\] staging table temporarily stores important data about catalog imports before this data is sent to the primary table.
locale: en-US
release: yokohama
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Inbound staging tables for Sourcing and Procurement Operations, Inbound staging tables for Source-to-Pay Operations, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Catalog Import staging table

The Catalog Import \[sn\_spend\_intg\_imp\_catalog\] staging table temporarily stores important data about catalog imports before this data is sent to the primary table.

|Fields|Data type|Description|
|------|---------|-----------|
|Available for countries|String|Countries where the product is available.|
|Available Units|String|Number of units of a product that are available.|
|Bundle|Boolean|Indicates whether the Product Model is of type bundle.|
|Bundled Components|String|Bundle model components as a json array.|
|Catalog id|String|Unique identifier for each catalog of the purchase order.|
|Category UNSPSC code|String| |
|Contract end date|String|Date on which the contract term ends.|
|Contract number|String| |
|Contract start date|String|Date on which the contract term starts.|
|Customer id|String|Unique identifier for the customer.|
|Delivery time|String|Estimated number of days it takes to ship a product to the customer.|
|Images|String|List of strings that specify the image URLs for the supplier product.|
|Manufacturer/publisher name|String|Name of the manufacturer or publisher.|
|Manufacturer/publisher part number \(MPN\)|String|Manufacturer or publisher’s unique identifier for the product.|
|Negotiated currency|String|Currency used in price negotiation.|
|Negotiated price|String|Unit price of a product as negotiated through a contract with the supplier .|
|Parent Bundle Part Number \(MPN/SKU\)|String|Manufacturer/publisher/supplier part number of the parent bundle.|
|Product attributes|String|Attributes of the product.|
|Product category|Reference|Reference to the Product category.|
|Product category name|String|Category of the product.|
|Product description|String|Description of the product.|
|Product name|String|Name of the product or service purchased from a supplier.|
|Provider|Reference| |
|Sales end date|String|Date when a product is discontinued or removed from the catalog.|
|Sales start date|String|Date when a product is published in the catalog.|
|Supplier id|String|Supplier ID for which the purchase order is generated.|
|Supplier part number|String|Supplier part number of the supplier product.|
|Third party import ID|String|Unique identifier for external data imports.|
|Third-party category|Reference|Reference to the Third Party category.|
|Unit|String|Unit or rate at which the product is sold by the supplier.|

**Parent Topic:**[Inbound staging tables for Sourcing and Procurement Operations](../concept/spo-inbound-staging-tables.md)

**Related topics**  


[CMDB Model Category Stage inbound staging table](spo-prod-cate-inbound-table.md)

[CMDB Service Model Stage inbound staging table](spo-serv-mod-inbound-table.md)

[CMN Location Stage inbound staging table](spo-loc-inbound-table.md)

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

