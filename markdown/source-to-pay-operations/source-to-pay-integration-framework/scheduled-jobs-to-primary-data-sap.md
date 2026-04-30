---
title: Scheduled jobs to look up primary data in SAP
description: You can schedule on-demand jobs to be run at specific intervals of time to fetch primary data from different SAP ERP sources into ServiceNow.
locale: en-US
release: yokohama
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Source-to-Pay integration with SAP, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Scheduled jobs to look up primary data in SAP

You can schedule on-demand jobs to be run at specific intervals of time to fetch primary data from different SAP ERP sources into ServiceNow.

Before you start the SAP ERP integration, you must configure the integration services record for target ERP source using the `sn_fcms_intg_service` table. The `sn_fcms_intg_service` table is a mapping table between sub flows and target ERP source. For more information on creating a integration service record, see [Configure integration services for SAP](../task/configure-service-maps-sap.md).

![Scheduled script execution](../../accounts-payable-operations/image/scheduled-script.png)

-   **[Run scheduled jobs in SAP](../task/run-scheduled-jobs-sap.md)**  
Run adhoc scheduled jobs to look up entity primary data from the target SAP ERP source.

**Parent Topic:**[Configure the Source-to-Pay integration with SAP](configuring-source-to-pay-sap-integration.md)

**Related topics**  


[ERP Source Configuration for SAP](erp-source-configuration-sap.md)

[Define ERP source configuration for SAP](../task/define-erp-source-sap.md)

[Configure integration services for SAP](../task/configure-service-maps-sap.md)

[Look up primary data in SAP](look-up-primary-data-sap.md)

[Manually execute flows or subflows in SAP \(Inbound\)](../task/manually-trigger-subflows-sap.md)

