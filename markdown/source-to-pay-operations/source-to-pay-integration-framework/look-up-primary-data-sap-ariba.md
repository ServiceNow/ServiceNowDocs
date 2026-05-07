---
title: Look up primary data in SAP Ariba
description: You can run a job to look up primary data from different ERP sources into ServiceNow.
locale: en-US
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

Before the ERP integration, configure the integration services record for the target ERP source using the `sn_fcms_intg_service` table. The `sn_fcms_intg_service` table is a mapping table between the subflows and targets the ERP source. For more information on creating an integration service record, see [Create Integration Service record](../../accounts-payable-operations/task/create-integration-service-record.md).

![Look up primary data in SAP Ariba](../../source-to-pay-operations/image/sap-ariba-lookup-primary-data.png "Look up primary data in SAP Ariba")

You can manually run jobs for the following entities:

|Entity|Description|Table name|
|------|-----------|----------|
|Legal entities|Lookup legal entities from SAP Ariba.|[Legal Entity Stage inbound staging table](../reference/spo-legal-entity-inbound-table.md)|
|FX Currency rates|Lookup FX rates from SAP Ariba.|[FX Rate Stage inbound staging table](../reference/spo-fx-rate-inbound-table.md)|
|Purchasing Orgs|Lookup purchasing orgs from SAP Ariba.|[Purchase Entity Stage inbound staging table](../reference/spo-purch-entity-inbound-table.md)|
|Currencies|Lookup currencies from SAP Ariba.|[FX Currency Stage inbound staging table](../reference/spo-fx-currency-inbound-table.md)|
|Payment Terms|Lookup payment terms from SAP Ariba.|[Payment Terms Stage inbound staging table](../reference/spo-pay-terms-inbound-table.md)|
|GL Accounts|Lookup GL accounts from SAP Ariba.|[GL Account Stage inbound staging table](../reference/spo-gl-account-inbound-table.md)|
|Cost Centers|Lookup cost centers from SAP Ariba.|[Cost Center Stage inbound staging table](../reference/spo-cost-center-inbound-table.md)|
|Departments|Lookup departments from SAP Ariba.|[Department Stage inbound staging table](../reference/spo-dept-inbound-table.md)|
|Suppliers|Lookup suppliers from SAP Ariba.|[Supplier Location inbound staging table](../reference/slo-supp-location-inbound-table.md)|
|Invoices|Lookup invoices from SAP Ariba.|[Invoice import inbound staging table](../reference/inbound-invoice-import-staging-table.md)|

**Parent Topic:**[Configure the Source-to-Pay integration with SAP Ariba](configuring-source-to-pay-sap-ariba-integration.md)

**Related topics**  


[ERP source configuration for SAP Ariba](erp-source-configuration-sap-ariba.md)

[Define ERP source configuration for SAP Ariba](../task/define-erp-source-sap-ariba.md)

[Configure integration services for SAP Ariba](configure-service-maps-sap-ariba.md)

