---
title: Look up primary data in SAP ECC and SAP S4 HANA
description: You can run a job to look up primary data \(for example, Currencies\) from different ERP sources into ServiceNow.
locale: en-US
release: xanadu
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2025-03-12"
reading_time_minutes: 4
breadcrumb: [Configuring the SAP ECC and SAP S4 HANA integration, Source-to-Pay integration with SAP ECC and SAP S4 HANA, Source-to-Pay integration with third-party applications, Source-to-Pay Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Look up primary data in SAP ECC and SAP S4 HANA

You can run a job to look up primary data \(for example, Currencies\) from different ERP sources into ServiceNow.

Before you start the ERP integration, you must configure the integration services record for the target ERP source using the `sn_fcms_intg_service` table. The `sn_fcms_intg_service` table is a mapping table between sub flows and target ERP source. For more information on creating an integration service record, see [Create Integration Service record](../../accounts-payable-operations/task/create-integration-service-record.md).

![Look up currencies in SAP ECC and SAP S4 HANA](../image/sap-integration-full-pull.png "Look up currencies in SAP ECC and SAP S4 HANA")

You can manually run jobs for the following entities:

|Entity|Table name|
|------|----------|
|Currencies|[FX Currency Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-fx-currency-inbound-table.md)|
|Legal entities|[Legal Entity Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-legal-entity-inbound-table.md)|
|FX Currency rates|[FX Rate Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-fx-rate-inbound-table.md)|
|Cost Centers|[Cost Center Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-cost-center-inbound-table.md)|
|Departments|[Department Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-dept-inbound-table.md)|
|Payment Terms|[Payment Terms Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-pay-terms-inbound-table.md)|
|Purchasing Organizations|[Purchase Entity Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-purch-entity-inbound-table.md)|
|GL Accounts|[GL Account Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-gl-account-inbound-table.md)|
|Plant Addresses|[CMN Location Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-loc-inbound-table.md)|
|Suppliers|[Supplier location inbound staging table](../../supplier-lifecycle-operations/reference/slo-supp-location-inbound-table.md)|
|Product Models|[Product Model Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-prod-mod-inbound-table.md)|
|Invoices|[Invoice import inbound staging table](../../sourcing-procurement-operations/reference/inbound-invoice-import-staging-table.md)|
|Unit of Measure||
|Product Categories|[Product Model Stage inbound staging table](../../sourcing-procurement-operations/reference/spo-prod-mod-inbound-table.md)|

## Transformation maps and subflows

To learn more about the Transformation maps and subflows, see [Source-to-Pay integration framework transform maps and subflows](../../sourcing-procurement-operations/concept/s2p-transform-maps-flows.md).

**Parent Topic:**[Configuring the Source-to-Pay integration with SAP ECC and SAP S4 HANA](configuring-source-to-pay-sap-integration.md)

**Related topics**  


[ERP Source Configuration for SAP ECC and SAP S4 HANA](erp-source-configuration-sap.md)

[Define ERP source configuration for SAP ECC and SAP S4 HANA](../task/define-erp-source-sap.md)

[Configure integration services for SAP ECC and SAP S4 HANA](../task/configure-service-maps-sap.md)

[Manually trigger flows or subflows in SAP ECC and SAP S4 HANA \(Inbound\)](../task/manually-trigger-subflows-sap.md)

[Scheduled jobs to look up primary data in SAP ECC and SAP S4 HANA](scheduled-jobs-to-primary-data-sap.md)

