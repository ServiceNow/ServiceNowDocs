---
title: Looking up primary data in Coupa
description: You can run a job to look up primary data from different ERP sources into ServiceNow
locale: en-US
release: yokohama
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure, Source-to-Pay integration with Coupa, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Looking up primary data in Coupa

You can run a job to look up primary data from different ERP sources into ServiceNow

Before you start the ERP integration, you must configure the integration services record for the target ERP source using the \[sn\_fcms\_intg\_service\] table. The \[sn\_fcms\_intg\_service\] table is a mapping table between sub flows and target ERP source. For more information on creating an integration service record, see [Create Integration Service record](../../accounts-payable-operations/task/create-integration-service-record.md).

![Look up primary data in Coupa](../image/coupa-integration-service.png "Look up primary data in Coupa")

You can manually run jobs for the following entities:

|Entity|Description|Table name|
|------|-----------|----------|
|Currencies|Look up currencies from Coupa.|[FX Currency Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-fx-currency-inbound-table.md)|
|FX Currency rates|Look up FX rates from Coupa.|[FX Rate Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-fx-rate-inbound-table.md)|
|Legal entities|Look up legal entities from Coupa.|[Legal Entity Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-legal-entity-inbound-table.md)|
|Purchase Line Shipment Details|Look up purchase line shipment details from Coupa.|[Purchase Requisition staging table](../../sourcing-procurement-operations/reference/purchase-requisition-staging-table.md)|
|Shipment Notices|Look up shipment notices from Coupa|-|
|Suppliers|Look up suppliers from Coupa.|[Supplier location inbound staging table](../../supplier-lifecycle-operations/reference/slo-supp-location-inbound-table.md)|
|Cost Centers|Look up cost centers from Coupa.|[Cost Center Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-cost-center-inbound-table.md)|
|Supplier Payment Information|Look up supplier payment information from Coupa.|[Supplier payment inbound staging table](../../supplier-lifecycle-operations/reference/slo-supp-payment-inbound-table.md)|
|Invoices|Look up invoices from Coupa.|[Invoice import inbound staging table](../../sourcing-procurement-operations/reference/inbound-invoice-import-staging-table.md)|
|Purchase Orders|Look up purchase orders from Coupa|[Inbound Purchase Order staging table](../../sourcing-procurement-operations/reference/spo-inbound-pur-order-table.md)|
|Invoice Payment Details|Look up invoice payment details from Coupa.|[Invoice payment detail import inbound table](../../accounts-payable-operations/reference/invoice-payment-detail-staging-table.md)|
|Receipts|Look up receipts from Coupa.|[Inbound Receipt staging table](../../sourcing-procurement-operations/reference/spo-inbound-receipt-table.md)|
|Product Models|Look up product models from Coupa.|[Product Model Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-prod-mod-inbound-table.md)|

**Parent Topic:**[Configure Source-to-Pay integration with Coupa](configuring-source-to-pay-coupa-integration.md)

**Related topics**  


[ERP Source Configuration for Coupa](erp-source-configuration-coupa.md)

[Define an ERP source configuration for Coupa](../task/define-erp-source-coupa.md)

[Configure integration services for Coupa](../task/configure-service-maps-coupa.md)

[Activate the schedule flows](../task/activate-schedule-flows-coupa.md)

