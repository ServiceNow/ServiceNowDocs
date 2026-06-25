---
title: Look up primary data in SAP
description: You can run a job to look up primary data \(for example, Currencies\) from different ERP sources into ServiceNow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/look-up-primary-data-sap.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, Source-to-Pay integration with SAP, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Look up primary data in SAP

You can run a job to look up primary data \(for example, Currencies\) from different ERP sources into ServiceNow.

Before you start the ERP integration, you must configure the integration services record for the target ERP source using the `sn_fcms_intg_service` table. The `sn_fcms_intg_service` table is a mapping table between sub flows and target ERP source. For more information on creating an integration service record, see [Create Integration Service record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/create-integration-service-record.md).

\[Omitted image "sap-integration-full-pull.png"\] Alt text: Look up currencies in SAP

You can manually run jobs for the following entities:

|Entity|Table name|
|------|----------|
|Currencies|[FX Currency Stage inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-fx-currency-inbound-table.md)|
|Legal entities|[Legal Entity Stage inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-legal-entity-inbound-table.md)|
|FX Currency rates|[FX Rate Stage inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-fx-rate-inbound-table.md)|
|Cost Centers|[Cost Center Stage inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-cost-center-inbound-table.md)|
|Departments|[Department Stage inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-dept-inbound-table.md)|
|Payment Terms|[Payment Terms Stage inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-pay-terms-inbound-table.md)|
|Purchasing Organizations|[Purchase Entity Stage inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-purch-entity-inbound-table.md)|
|GL Accounts|[GL Account Stage inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-gl-account-inbound-table.md)|
|Plant Addresses|[CMN Location Stage inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-loc-inbound-table.md)|
|Suppliers|[Supplier Location inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/slo-supp-location-inbound-table.md)|
|Product Models|[Product Model Stage inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-prod-mod-inbound-table.md)|
|Invoices|[Invoice import inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/inbound-invoice-import-staging-table.md)|
|Unit of Measure|[Unit of Measure inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/unit-measure-inbound-staging-table.md)|
|Product Categories|[Product Model Stage inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-prod-mod-inbound-table.md)|

## Transformation maps and subflows

To learn more about the Transformation maps and subflows, see [Source-to-Pay integration framework transform maps and subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/s2p-transform-maps-flows.md).

**Parent Topic:**[Configure the Source-to-Pay integration with SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/configuring-source-to-pay-sap-integration.md)

**Related topics**  


[ERP Source Configuration for SAP]()

[Define ERP source configuration for SAP]()

[Configure integration services for SAP]()

[Manually execute flows or subflows in SAP \(Inbound\)]()

[Scheduled jobs to look up primary data in SAP]()

