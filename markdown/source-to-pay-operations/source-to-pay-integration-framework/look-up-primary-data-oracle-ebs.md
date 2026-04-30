---
title: Look up primary data in Oracle EBS
description: You can run a job to look up primary data from different ERP sources into ServiceNow.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, Source-to-Pay integration with Oracle EBS, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Look up primary data in Oracle EBS

You can run a job to look up primary data from different ERP sources into ServiceNow.

Before you start the ERP integration, you must configure the integration services record for the target ERP source using the `sn_fcms_intg_service` table. The `sn_fcms_intg_service` table is a mapping table between sub flows and target ERP source. For more information on creating an integration service record, see [Create Integration Service record](../../accounts-payable-operations/task/create-integration-service-record.md).

![Look up primary data in Oracle EBS](../image/oracle-ebs-integration-service.png "Look up primary data in Oracle EBS")

You can manually run jobs for the following entities:

|Entity|Description|Table name|
|------|-----------|----------|
|Cost Centers|Lookup cost centers from Oracle EBS|[Cost Center Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-cost-center-inbound-table.md)|
|Product Models|Lookup product models from Oracle EBS.|[Product Model Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-prod-mod-inbound-table.md)|
|Payment Terms|Lookup payment terms from Oracle EBS.|[Payment Terms Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-pay-terms-inbound-table.md)|
|Purchasing Orgs|Lookup purchasing orgs from Oracle EBS.|[Purchase Entity Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-purch-entity-inbound-table.md)|
|Departments|Lookup departments from Oracle EBS.|[Department Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-dept-inbound-table.md)|
|GL Accounts|Lookup GL accounts from Oracle EBS.|[GL Account Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-gl-account-inbound-table.md)|
|Currencies|Lookup currencies from Oracle EBS.|[FX Currency Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-fx-currency-inbound-table.md)|
|FX Currency rates|Lookup FX rates from Oracle EBS.|[FX Rate Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-fx-rate-inbound-table.md)|
|Invoice Payment Details|Lookup invoice payment details from Oracle EBS.|[Invoice payment detail import inbound table](../../accounts-payable-operations/reference/invoice-payment-detail-staging-table.md)|
|Suppliers|Lookup suppliers from Oracle EBS.|[Supplier Location inbound staging table](../../supplier-lifecycle-operations/reference/slo-supp-location-inbound-table.md)|
|Plant addresses|Lookup plant addresses from Oracle EBS.|[CMN Location Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-loc-inbound-table.md)|
|Legal entities|Lookup legal entities from Oracle EBS.|[Legal Entity Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-legal-entity-inbound-table.md)|
|Invoices|Lookup invoices from Oracle EBS.|[Invoice import inbound staging table](../../sourcing-procurement-operations/reference/inbound-invoice-import-staging-table.md)|

## Transformation maps and subflows

To learn more about the Transformation maps and subflows, see [Source-to-Pay integration framework transform maps and subflows](../../sourcing-procurement-operations/concept/s2p-transform-maps-flows.md).

**Parent Topic:**[Configure the Source-to-Pay integration with Oracle EBS](configuring-source-to-pay-oracle-ebs-integration.md)

**Related topics**  


[ERP source configuration for Oracle EBS](erp-source-configuration-oracle.md)

[Define ERP source configuration for Oracle EBS](../task/define-erp-source-oracle.md)

[Configure integration services for Oracle EBS](../task/configure-service-maps-oracle-ebs.md)

[Load data to ERP user-mapping table for Oracle EBS](../task/load-data-erp-user-mapping-oracle-ebs.md)

[Scheduled jobs to look up primary data in Oracle EBS](scheduled-jobs-to-primary-data-oracle-ebs.md)

