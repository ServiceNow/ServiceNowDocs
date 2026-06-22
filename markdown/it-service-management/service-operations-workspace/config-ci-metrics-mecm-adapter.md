---
title: Configuring CI metrics for Microsoft Endpoint Configuration Manager for Investigation
description: Configure the display of the metrics for Microsoft Endpoint Configuration Manager for Investigation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/service-operations-workspace/config-ci-metrics-mecm-adapter.html
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setting up investigation framework using Microsoft Endpoint Configuration Manager for Investigation, Setting up Investigation Framework in Service Operations Workspace, Setting up integrations in Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Configuring CI metrics for Microsoft Endpoint Configuration Manager for Investigation

Configure the display of the metrics for Microsoft Endpoint Configuration Manager for Investigation.

You must ensure the following requirements:

-   Microsoft Endpoint Configuration Manager for Investigation \(sn\_mecm\_adapter\) application must be installed along with the investigation framework applications. For more information, see [Install Microsoft Endpoint Configuration Manager\(MECM\) for Investigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/install-mecm-adapter.md) and [Components installed with Microsoft Endpoint Configuration Manager for Investigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/components-installed-mecm-adapter.md).
-   Microsoft Endpoint Configuration Manager Spoke \[sn\_ms\_epcfgmgr\_spk\] must be installed and configured. For more information, see [Microsoft Endpoint Configuration Manager spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/ms-endpoint.md) and [Microsoft SCCM integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/c_MicrosoftSCCMIntegration.md).
-   Microsoft Endpoint Configuration Manager server must be logged in using the Microsoft remote desktop.

**Note:** You can configure the delay time in milliseconds between two consecutive Microsoft Endpoint Configuration Manager queries that are submitted to the Microsoft Endpoint Configuration Manager server to fetch and display the metrics, using the property **Specify the delay in milliseconds between two MECM query submissions.** \(**sn\_mecm\_adapter.request\_query\_delay**\). The default value is 10000.

-   **[Configure system overview - msinfo32 metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/config-system-msinfo32-metrics.md)**  
Configure the system overview - msinfo32 metrics for Microsoft Endpoint Configuration Manager for Investigation \(MECM\).
-   **[Configure system overview - dsregcmd metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/config-system-dsregcmd-metrics.md)**  
Configure the system overview - dsregcmd metrics for Microsoft Endpoint Configuration Manager for Investigation \(MECM\).
-   **[Configure asset utilization metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/configure-asset-utilization-mecm.md)**  
Configure the display of the asset utilization metrics for Microsoft Endpoint Configuration Manager for Investigation.
-   **[Configure processes metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/configure-processes-metrics-mecm.md)**  
Configure the top processes by CPU and top processes by memory metrics for Microsoft Endpoint Configuration Manager for Investigation.
-   **[Configure services metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/configure-services-metrics.md)**  
Configure the services metrics for Microsoft Endpoint Configuration Manager for Investigation \(MECM\).
-   **[Configure logged in users metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/config-logged-in-users-metrics.md)**  
Configure the display of the logged in users metrics for Microsoft Endpoint Configuration Manager for Investigation.
-   **[Configure Installed application metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/config-install-app-metrics.md)**  
Configure the display of the installed application metrics for Microsoft Endpoint Configuration Manager for Investigation.
-   **[Configure remedial action - Restart Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/config-ra-restart-service.md)**  
Configure the Restart Service remedial action for Microsoft Endpoint Configuration Manager for Investigation \(MECM\).
-   **[Configure remedial actions - End Process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/config-ra-end-process.md)**  
Configure the End Process remedial action for Microsoft Endpoint Configuration Manager for Investigation \(MECM\).
-   **[Create a script in Microsoft Endpoint Configuration Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/create-mecm-script.md)**  
Create a script in the Microsoft Endpoint Configuration Manager to configure the display of the processes metrics on the **Investigation** tab of the Incident record.
-   **[Extend hardware inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/extend-hardware-entity.md)**  
Extend the hardware inventory to add the CMPivot entity on the CMPivot entity list in the Microsoft Endpoint Configuration Manager.
-   **[Verify a CMPivot entity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/verify-cmpivot-entity.md)**  
Verify a CMPivot entity and its attributes to configure the display of the CI metrics information on the Investigation tab of the Incident record.

**Parent Topic:**[Setting up investigation framework using Microsoft Endpoint Configuration Manager for Investigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/set-up-investigate-fw-mecm.md)

