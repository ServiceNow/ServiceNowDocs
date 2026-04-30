---
title: Scheduled jobs to look up primary data in SAP ECC and SAP S4 HANA
description: You can schedule on-demand jobs to be run at specific intervals of time to fetch primary data from different SAP ECC and SAP S4 HANA ERP sources into ServiceNow.
locale: en-US
release: xanadu
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring the SAP ECC and SAP S4 HANA integration, Source-to-Pay integration with SAP ECC and SAP S4 HANA, Source-to-Pay integration with third-party applications, Source-to-Pay Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Scheduled jobs to look up primary data in SAP ECC and SAP S4 HANA

You can schedule on-demand jobs to be run at specific intervals of time to fetch primary data from different SAP ECC and SAP S4 HANA ERP sources into ServiceNow.

Before you start the SAP ECC and SAP S4 HANA ERP integration, you must configure the integration services record for target ERP source using the `sn_fcms_intg_service` table. The `sn_fcms_intg_service` table is a mapping table between sub flows and target ERP source. For more information on creating a integration service record, see [Configure integration services for SAP ECC and SAP S4 HANA](../task/configure-service-maps-sap.md).

![Scheduled script execution](../../accounts-payable-operations/image/scheduled-script.png)

-   **[Run scheduled jobs in SAP ECC and SAP S4 HANA](../task/run-scheduled-jobs-sap.md)**  
Run adhoc scheduled jobs to look up entity primary data from the target SAP ECC and SAP S4 HANA ERP source.

**Parent Topic:**[Configuring the Source-to-Pay integration with SAP ECC and SAP S4 HANA](configuring-source-to-pay-sap-integration.md)

**Related topics**  


[ERP Source Configuration for SAP ECC and SAP S4 HANA](erp-source-configuration-sap.md)

[Define ERP source configuration for SAP ECC and SAP S4 HANA](../task/define-erp-source-sap.md)

[Configure integration services for SAP ECC and SAP S4 HANA](../task/configure-service-maps-sap.md)

[Look up primary data in SAP ECC and SAP S4 HANA](look-up-primary-data-sap.md)

[Manually trigger flows or subflows in SAP ECC and SAP S4 HANA \(Inbound\)](../task/manually-trigger-subflows-sap.md)

