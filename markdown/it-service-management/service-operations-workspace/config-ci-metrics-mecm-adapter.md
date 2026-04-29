---
title: Configuring CI metrics for Microsoft Endpoint Configuration Manager for Investigation
description: Configure the display of the metrics for Microsoft Endpoint Configuration Manager for Investigation.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Investigation using Microsoft Endpoint Configuration Manager, Setting up Investigation Framework in Service Operations Workspace, Setting up integrations in Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Configuring CI metrics for Microsoft Endpoint Configuration Manager for Investigation

Configure the display of the metrics for Microsoft Endpoint Configuration Manager for Investigation.

You must ensure the following requirements:

-   Microsoft Endpoint Configuration Manager for Investigation \(sn\_mecm\_adapter\) application must be installed along with the investigation framework applications. For more information, see [Install Microsoft Endpoint Configuration Manager\(MECM\) for Investigation](../task/install-mecm-adapter.md) and [Components installed with Microsoft Endpoint Configuration Manager for Investigation](../reference/components-installed-mecm-adapter.md).
-   Microsoft Endpoint Configuration Manager Spoke \[sn\_ms\_epcfgmgr\_spk\] must be installed and configured. For more information, see [Microsoft Endpoint Configuration Manager spoke](https://www.servicenow.com/docs/access?context=ms-endpoint&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) and [Microsoft SCCM integration](https://www.servicenow.com/docs/access?context=c_MicrosoftSCCMIntegration&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Microsoft Endpoint Configuration Manager server must be logged in using the Microsoft remote desktop.

**Note:** You can configure the delay time in milliseconds between two consecutive Microsoft Endpoint Configuration Manager queries that are submitted to the Microsoft Endpoint Configuration Manager server to fetch and display the metrics, using the property **Specify the delay in milliseconds between two MECM query submissions.** \(**sn\_mecm\_adapter.request\_query\_delay**\). The default value is 10000.

-   **[Configure system overview - msinfo32 metrics](../task/config-system-msinfo32-metrics.md)**  
Configure the system overview - msinfo32 metrics for Microsoft Endpoint Configuration Manager for Investigation \(MECM\).
-   **[Configure system overview - dsregcmd metrics](../task/config-system-dsregcmd-metrics.md)**  
Configure the system overview - dsregcmd metrics for Microsoft Endpoint Configuration Manager for Investigation \(MECM\).
-   **[Configure asset utilization metrics](../task/configure-asset-utilization-mecm.md)**  
Configure the display of the asset utilization metrics for Microsoft Endpoint Configuration Manager for Investigation.
-   **[Configure processes metrics](../task/configure-processes-metrics-mecm.md)**  
Configure the top processes by CPU and top processes by memory metrics for Microsoft Endpoint Configuration Manager for Investigation.
-   **[Configure services metrics](../task/configure-services-metrics.md)**  
Configure the services metrics for Microsoft Endpoint Configuration Manager for Investigation \(MECM\).
-   **[Configure logged in users metrics](../task/config-logged-in-users-metrics.md)**  
Configure the display of the logged in users metrics for Microsoft Endpoint Configuration Manager for Investigation.
-   **[Configure Installed application metrics](../task/config-install-app-metrics.md)**  
Configure the display of the installed application metrics for Microsoft Endpoint Configuration Manager for Investigation.
-   **[Configure remedial action - Restart Service](../task/config-ra-restart-service.md)**  
Configure the Restart Service remedial action for Microsoft Endpoint Configuration Manager for Investigation \(MECM\).
-   **[Configure remedial actions - End Process](../task/config-ra-end-process.md)**  
Configure the End Process remedial action for Microsoft Endpoint Configuration Manager for Investigation \(MECM\).
-   **[Create a script in Microsoft Endpoint Configuration Manager](../task/create-mecm-script.md)**  
Create a script in the Microsoft Endpoint Configuration Manager to configure the display of the processes metrics on the **Investigation** tab of the Incident record.
-   **[Extend hardware inventory](../task/extend-hardware-entity.md)**  
Extend the hardware inventory to add the CMPivot entity on the CMPivot entity list in the Microsoft Endpoint Configuration Manager.
-   **[Verify a CMPivot entity](../task/verify-cmpivot-entity.md)**  
Verify a CMPivot entity and its attributes to configure the display of the CI metrics information on the Investigation tab of the Incident record.

**Parent Topic:**[Setting up investigation framework using Microsoft Endpoint Configuration Manager for Investigation](set-up-investigate-fw-mecm.md)

