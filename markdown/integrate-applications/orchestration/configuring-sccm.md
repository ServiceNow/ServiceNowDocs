---
title: Configuring SCCM
description: Follow the SCCM configuration procedures in the order shown.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Client software distribution from SCCM, Client Software Distribution, Orchestration applications, Classic Orchestration, Workflow Data Fabric]
---

# Configuring SCCM

Follow the SCCM configuration procedures in the order shown.

-   **[Configure the Application Administrator role on the SCCM server](../task/t-config-SCCM-deployment-manager.md)**  
To deploy software using ServiceNow® Client Software Distribution \(CSD\), ensure that an SCCM administrative user has the correct permissions to deploy software and that PowerShell is properly configured.
-   **[Update the SCCM cmdlet libraries](../task/t-update-sccm-cmdlet-libraries.md)**  
Ensure that the System Center Configuration Manager SCCM Cmdlet Library is up-to-date.
-   **[Configure the MID Server for SCCM activities](../../../administer/orchestration-activities/task/t_ConfigMIDServerForSCCMActivities.md)**  
To use a MID Server with Microsoft System Center Configuration Management \(SCCM\) activities, configure it to communicate with the SCCM server.
-   **[Create Windows credentials for SCCM deployments](../task/t_CreateWinCredSCCM.md)**  
Microsoft System Center Configuration Manager \(SCCM\) requires the appropriate credentials to deploy applications using the Client Software Distribution application.
-   **[Retrieve SCCM data for client software distribution](../task/t_RetrieveSCCMDataClientSWDist.md#)**  
Retrieve the collections and the list of applications available for deployment from your SCCM servers.
-   **[Set up a software model for an SCCM application](../task/t_CreateSWModelSCCMApp.md)**  
Using the applications discovered on the SCCM server, set up a software model used by the Software Asset Management application to manage licenses.
-   **[Define an SCCM configuration](../task/t_ConfigureSCCMCollections.md)**  
To create catalog items for SCCM software deployment or to configure your instance to revoke software through SCCM, you must first associate that software with a collection through an SCCM configuration.
-   **[Create a catalog item for an SCCM application](../task/t_CreateCatItemSCCMApp.md)**  
Using the applications discovered on the SCCM server, create a catalog item for an application you want to offer for distribution from the service catalog.

**Parent Topic:**[Client software distribution from SCCM](c_CSDFromAnSCCMHost.md)

