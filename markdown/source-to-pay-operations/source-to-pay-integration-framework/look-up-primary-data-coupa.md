---
title: Looking up primary data in Coupa
description: You can run a job to look up primary data from different ERP sources into ServiceNow
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/look-up-primary-data-coupa.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Source-to-Pay integration with Coupa, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Looking up primary data in Coupa

You can run a job to look up primary data from different ERP sources into ServiceNow

Before you start the ERP integration, you must configure the integration services record for the target ERP source using the \[sn\_fcms\_intg\_service\] table. The \[sn\_fcms\_intg\_service\] table is a mapping table between sub flows and target ERP source. For more information on creating an integration service record, see [Create Integration Service record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/create-integration-service-record.md).

\[Omitted image "coupa-integration-service.png"\] Alt text: Look up primary data in Coupa

You can manually run jobs for the following entities:

|Entity|Description|Table name|
|------|-----------|----------|
|Currencies|Look up currencies from Coupa.|[FX Currency Stage inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-fx-currency-inbound-table.md)|
|FX Currency rates|Look up FX rates from Coupa.|[FX Rate Stage inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-fx-rate-inbound-table.md)|
|Legal entities|Look up legal entities from Coupa.|[Legal Entity Stage inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-legal-entity-inbound-table.md)|
|Purchase Line Shipment Details|Look up purchase line shipment details from Coupa.|[Purchase Requisition staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/purchase-requisition-staging-table.md)|
|Shipment Notices|Look up shipment notices from Coupa|-|
|Suppliers|Look up suppliers from Coupa.|[Supplier Location inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/slo-supp-location-inbound-table.md)|
|Cost Centers|Look up cost centers from Coupa.|[Cost Center Stage inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-cost-center-inbound-table.md)|
|Supplier Payment Information|Look up supplier payment information from Coupa.|[Supplier Payment inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/slo-supp-payment-inbound-table.md)|
|Invoices|Look up invoices from Coupa.|[Invoice import inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/inbound-invoice-import-staging-table.md)|
|Purchase Orders|Look up purchase orders from Coupa|[Purchase Order inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-inbound-pur-order-table.md)|
|Invoice Payment Details|Look up invoice payment details from Coupa.|[Invoice payment detail import inbound table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/invoice-payment-detail-staging-table.md)|
|Receipts|Look up receipts from Coupa.|[Receipt inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-inbound-receipt-table.md)|
|Product Models|Look up product models from Coupa.|[Product Model Stage inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-prod-mod-inbound-table.md)|

**Parent Topic:**[Configure Source-to-Pay integration with Coupa](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/configuring-source-to-pay-coupa-integration.md)

**Related topics**  


[ERP Source Configuration for Coupa]()

[Define an ERP source configuration for Coupa]()

[Configure integration services for Coupa]()

[Activate the schedule flows]()

