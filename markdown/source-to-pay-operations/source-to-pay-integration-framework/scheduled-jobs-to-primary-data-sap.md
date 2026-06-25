---
title: Scheduled jobs to look up primary data in SAP
description: You can schedule on-demand jobs to be run at specific intervals of time to fetch primary data from different SAP ERP sources into ServiceNow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/scheduled-jobs-to-primary-data-sap.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Source-to-Pay integration with SAP, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Scheduled jobs to look up primary data in SAP

You can schedule on-demand jobs to be run at specific intervals of time to fetch primary data from different SAP ERP sources into ServiceNow.

Before you start the SAP ERP integration, you must configure the integration services record for target ERP source using the `sn_fcms_intg_service` table. The `sn_fcms_intg_service` table is a mapping table between sub flows and target ERP source. For more information on creating a integration service record, see [Configure integration services for SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/configure-service-maps-sap.md).

\[Omitted image "scheduled-script.png"\] Alt text: Scheduled script execution

-   **[Run scheduled jobs in SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/run-scheduled-jobs-sap.md)**  
Run adhoc scheduled jobs to look up entity primary data from the target SAP ERP source.

**Parent Topic:**[Configure the Source-to-Pay integration with SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/configuring-source-to-pay-sap-integration.md)

**Related topics**  


[ERP Source Configuration for SAP]()

[Define ERP source configuration for SAP]()

[Configure integration services for SAP]()

[Look up primary data in SAP]()

[Manually execute flows or subflows in SAP \(Inbound\)]()

