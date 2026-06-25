---
title: Look up primary data in SAP Ariba
description: You can run a job to look up primary data from different ERP sources into ServiceNow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/look-up-primary-data-sap-ariba.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Source-to-Pay integration with SAP Ariba, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Look up primary data in SAP Ariba

You can run a job to look up primary data from different ERP sources into ServiceNow.

Before the ERP integration, configure the integration services record for the target ERP source using the `sn_fcms_intg_service` table. The `sn_fcms_intg_service` table is a mapping table between the subflows and targets the ERP source. For more information on creating an integration service record, see [Create Integration Service record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/create-integration-service-record.md).

\[Omitted image "sap-ariba-lookup-primary-data.png"\] Alt text: Look up primary data in SAP Ariba

You can manually run jobs for the following entities:

|Entity|Description|Table name|
|------|-----------|----------|
|Legal entities|Lookup legal entities from SAP Ariba.|[Legal Entity Stage inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-legal-entity-inbound-table.md)|
|FX Currency rates|Lookup FX rates from SAP Ariba.|[FX Rate Stage inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-fx-rate-inbound-table.md)|
|Purchasing Orgs|Lookup purchasing orgs from SAP Ariba.|[Purchase Entity Stage inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-purch-entity-inbound-table.md)|
|Currencies|Lookup currencies from SAP Ariba.|[FX Currency Stage inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-fx-currency-inbound-table.md)|
|Payment Terms|Lookup payment terms from SAP Ariba.|[Payment Terms Stage inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-pay-terms-inbound-table.md)|
|GL Accounts|Lookup GL accounts from SAP Ariba.|[GL Account Stage inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-gl-account-inbound-table.md)|
|Cost Centers|Lookup cost centers from SAP Ariba.|[Cost Center Stage inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-cost-center-inbound-table.md)|
|Departments|Lookup departments from SAP Ariba.|[Department Stage inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-dept-inbound-table.md)|
|Suppliers|Lookup suppliers from SAP Ariba.|[Supplier Location inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/slo-supp-location-inbound-table.md)|
|Invoices|Lookup invoices from SAP Ariba.|[Invoice import inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/inbound-invoice-import-staging-table.md)|

**Parent Topic:**[Configure the Source-to-Pay integration with SAP Ariba](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/configuring-source-to-pay-sap-ariba-integration.md)

**Related topics**  


[ERP source configuration for SAP Ariba]()

[Define ERP source configuration for SAP Ariba]()

[Configure integration services for SAP Ariba]()

