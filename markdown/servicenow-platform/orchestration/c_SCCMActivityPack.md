---
title: SCCM activity pack
description: The Microsoft System Center Configuration Management \(SCCM\) activity pack provides Orchestration activities you can use to manage software deployments and collections on an SCCM server.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# SCCM activity pack

The Microsoft System Center Configuration Management \(SCCM\) activity pack provides Orchestration activities you can use to manage software deployments and collections on an SCCM server.

You can use SCCM Orchestration activities to deploy and revoke software from an SCCM server or manage user and device collections. The system manages software on an SCCM server using Orchestration activities and workflows.

Client software distribution requires:

-   SCCM 2012 R2 and later.
-   Powershell 3.x.
-   Powershell Remoting enabled.
-   The Windows PowerShell x86 execution policy must be set to unrestricted mode.
-   Latest version of the SCCM **cmdlet** library installed on the SCCM server.
-   Use the credentials to log onto the SCCM Server and connect via Windows PowerShell from the System Center Configuration Manager console at least once to set the path variable for that credential.

-   **[Request SCCM activities](../../../product/orchestration/task/t_ActivateSysCentrConfigMgrActiv.md)**  
The Orchestration - System Center Configuration Manager plugin installs the SCCM activity pack that deploys software from an SCCM host and manages user and device collections.
-   **[Configure the MID Server for SCCM activities](../task/t_ConfigMIDServerForSCCMActivities.md)**  
To use a MID Server with Microsoft System Center Configuration Management \(SCCM\) activities, configure it to communicate with the SCCM server.
-   **[Add to Device Collection activity](../reference/r_AddToDeviceCollectionActivity.md)**  
The Add to Device Collection activity adds the specified device into a Microsoft System Center Configuration Manager \(SCCM\) device collection.
-   **[Add to User Collection activity](../reference/r_AddToUserCollectionActivity.md)**  
The Add to User Collection activity adds a user to a Microsoft System Center Configuration Manager \(SCCM\) user collection.
-   **[Get Applications activity](../reference/r_GetApplicationsActivity.md)**  
The Get Applications activity returns a list of all the applications available on a Microsoft System Center Configuration Manager \(SCCM\) server.
-   **[Get Deployments activity](../reference/r_GetDeploymentsActivity.md)**  
The Get Deployments activity returns the list of deployments performed by Orchestration using a Microsoft System Center Configuration Manager \(SCCM\) server.
-   **[Get Device Collections activity](../reference/r_GetDeviceCollectionsActivity.md)**  
The Get Device Collections activity returns the list of available device collections on a Microsoft System Center Configuration Manager \(SCCM\) host.
-   **[Get User Collections activity](../reference/r_GetUserCollectionsActivity.md)**  
The Get User Collections activity returns the list of available user collections on a Microsoft System Center Configuration Manager \(SCCM\) server.
-   **[Is Device in Collection activity](../reference/device-exists-sccm-collection.md)**  
This activity verifies if a device exists in an SCCM device collection.
-   **[Is User in Collection activity](../reference/user-exists-sccm-collection.md)**  
This activity verifies if a user exists in an SCCM user collection.
-   **[Remove from Device Collection activity](../reference/r_RemoveFmDevicCollectionActivity.md)**  
The Remove from Device Collection activity removes a device from a Microsoft System Center Configuration Manager \(SCCM\) device collection.
-   **[Remove from User Collection activity](../reference/r_RemoveFromUserCollectionActivity.md)**  
The Remove from User Collection activity removes a user from a Microsoft System Center Configuration Manager \(SCCM\) user collection.

**Parent Topic:**[Orchestration activity packs](c_OrchestrationActivityPacks.md)

