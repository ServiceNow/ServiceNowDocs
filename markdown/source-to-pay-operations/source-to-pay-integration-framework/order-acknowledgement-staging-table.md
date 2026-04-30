---
title: Order Acknowledgement staging table
description: The Order Acknowledgment \[sn\_spend\_intg\_imp\_purchase\_order\_ack\] staging table temporarily stores important data about order acknowledgements before this data is sent to the primary table.
locale: en-US
release: yokohama
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Inbound staging tables for Sourcing and Procurement Operations, Inbound staging tables for Source-to-Pay Operations, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Order Acknowledgement staging table

The Order Acknowledgment \[sn\_spend\_intg\_imp\_purchase\_order\_ack\] staging table temporarily stores important data about order acknowledgements before this data is sent to the primary table.

|Field|Data type|Description|
|-----|---------|-----------|
|Customer id|String|Unique identifier for a customer.|
|Estimated arrival date|String|Date on which the order is expected to arrive.|
|Purchase order line number|String|Line number against which the receipt of the product is acknowledged.|
|Purchase order number|String|Unique number for the purchase order.|
|Sales order line number|String|Unique identifier for each item on a sales order.|
|Sales order number|String|Unique identifier for a customer's purchase.|
|Status code|String|Code indicating the current status.|
|Status message|String|A message that indicates the current status.|
|Supplier id|String|Unique identifier for the supplier.|
|Third party import ID|String|Unique identifier for external data imports.|

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

[Inbound Cost Allocation staging table](spo-cost-alloc-inbound-table.md)

[Inbound Invoice staging table](spo-inbound-invoice-table.md)

[Inbound Purchase Order staging table](spo-inbound-pur-order-table.md)

[Inbound Purchase Order Line staging table](spo-inbound-pol-table.md)

[Inbound Receipt staging table](spo-inbound-receipt-table.md)

[Legal Entity Stage inbound staging table](spo-legal-entity-inbound-table.md)

[Office Location Stage inbound staging table](spo-office-loc-inbound-table.md)

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

