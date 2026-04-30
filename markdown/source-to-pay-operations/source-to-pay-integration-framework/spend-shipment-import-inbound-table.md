---
title: Spend Shipment Import inbound staging table
description: The Spend Shipment Import inbound \[sn\_spend\_intg\_imp\_shipment\] staging table temporarily stores important data about spend shipment imports before this data is sent to the primary table.
locale: en-US
release: zurich
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Inbound staging tables for Sourcing and Procurement Operations, Inbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
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

[Fixed asset details stage inbound table](fixed-asset-details-stage-inbound-table.md)

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

[Shipment Error staging table](shipment-error-staging-table.md)

[Supplier Product Stage inbound staging table](spo-supp-prod-inbound-table.md)

[Third Party Sourcing Registration staging table](third-party-sourcing-registration-staging-table.md)

[Third Party Unit Mapping staging table](third-party-unit-mapping-staging-table.md)

[Third Party Unit staging table](third-party-unit-staging-table.md)

[Unit of Measure inbound staging table](unit-measure-inbound-staging-table.md)

