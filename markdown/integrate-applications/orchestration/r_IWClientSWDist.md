---
title: Installed with client software distribution
description: Several types of components are installed with client software distribution \(CSD\).These tables are installed with the Orchestration - Client Software Distribution plugin \(com.snc.orchestration.client\_sf\_distribution\).These plugins are installed with the Orchestration - Client Software Distribution plugin, if they are not already active.These roles are installed with the Orchestration - Client Software Distribution plugin.These script includes are installed with the Orchestration - Client Software Distribution pluginProperties for client software distribution \(CSD\) manage the installation status of requested software deployments and configure scheduled Discoveries.These workflows are installed with the Orchestration - Client Software Distribution plugin
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Client Software Distribution, Orchestration applications, Classic Orchestration, Workflow Data Fabric]
---

# Installed with client software distribution

Several types of components are installed with client software distribution \(CSD\).

**Parent Topic:**[Client Software Distribution](../concept/c_ClientSoftwareDistribution.md)

## Tables installed with client software distribution

These tables are installed with the Orchestration - Client Software Distribution plugin \(com.snc.orchestration.client\_sf\_distribution\).

|Table|Description|
|-----|-----------|
|Client Software Distribution Catalog Item \[sn\_client\_sf\_dist\_cat\_item\]|Contains all catalog items created for client software distribution. This table extends the Catalog Item \[sc\_cat\_item\] table.|
|Client Software Distribution Software Request \[sn\_client\_sf\_dist\_req\_software\]|Contains all requested software, and their statuses.|
|Client Software Distribution Application \[sn\_client\_sf\_dist\_application\]|Contains all discovered CSD applications.|
|Client Software Distribution Provider \[sn\_client\_sf\_dist\_provider\]|Contains all software distribution providers.|
|Client Software Distribution Extension Key \[sn\_client\_sf\_dist\_extension\_key\]|Contains the predefined CSD extension keys.|
|Client Software Distribution Extension Point \[sn\_client\_sf\_dist\_extension\_point\]|Contains the customization script for the extension keys.|
|Client Software Distribution Software Configuration \[sn\_client\_sf\_dist\_software\_config\]|Base table for all software provider configurations.|
|SCCM Server Instance \[sn\_client\_sf\_dist\_cmdb\_ci\_sccm\_server\]|Contains all SCCM server instances. This table extends the Configuration Item \[cmdb\_ci\] table.|
|SCCM Application \[sn\_client\_sf\_dist\_sccm\_application\]|Contains all discovered SCCM applications. This table extends the Client Software Distribution Application \[sn\_client\_sf\_dist\_application\] table.|
|SCCM Application Catalog Item \[sn\_client\_sf\_dist\_sccm\_app\_cat\_item\]|Contains all catalog items created for SCCM applications. This table extends the Client Software Distribution Catalog Item \[sn\_client\_sf\_dist\_cat\_item\] table.|
|SCCM Collection \[sn\_client\_sf\_dist\_sccm\_collection\]|Contains all discovered SCCM collections. Contains all discovered SCCM collections.|
|SCCM Deployment \[sn\_client\_sf\_dist\_sccm\_deployment\]|Contains all discovered SCCM deployments. Contains all discovered SCCM deployments.|
|SCCM Configuration \[sn\_client\_sf\_dist\_sccm\_sf\_config\]|Contains the SCCM application, install and uninstall collections, and Discovery model. This table extends the Client Software Distribution Software Configuration \[sn\_client\_sf\_dist\_software\_config\]|

## Plugins installed with client software distribution

These plugins are installed with the Orchestration - Client Software Distribution plugin, if they are not already active.

For instructions on requesting activation of Client Software Distribution \(CSD\) see [Request client software distribution](../task/t_ActivateClientSWDistribution.md).

<table id="table_zvn_hpc_ks"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Orchestration - System Center Configuration Manager\[com.snc.orchestration.sccm\_mgnt\]

</td><td>

Installs the custom SCCM Orchestration activities that do work on the SCCM target host.

</td></tr><tr><td>

Orchestration - Asset Lease Management \[com.snc.orchestration.asset\_lease\_management\]

</td><td>

Installs the [lease functionality](../task/t_CreateLicsAndCountsForDistSW.md#) for software distributed through the Service Catalog. This includes starting, stopping, and extending leases.

</td></tr><tr><td>

Service Catalog Scoped API

 \[com.glideapp.servicecatalog.scoped.api\]

</td><td>

Installs the API to support application creation in the Service Catalog.

</td></tr><tr><td>

Software Asset Management\[com.snc.software\_asset\_management\]

</td><td>

Provides the ability to manage software assets, including the reconciliation of entitlements to licenses for named users, workstation, and enterprise software agreements.

</td></tr></tbody>
</table>## Roles installed with client software distribution

These roles are installed with the Orchestration - Client Software Distribution plugin.

<table id="table_h3t_4pc_ks"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains Roles

</th></tr></thead><tbody><tr><td>

Client software distribution admin\[sn\_client\_sf\_dist.csd\_admin\]

</td><td>

Administrator role for managing client software distribution application.

</td><td>

-   sam
-   agent\_admin
-   report\_admin
-   catalog\_admin
-   itil
-   workflow\_admin

</td></tr></tbody>
</table>## Script includes installed with client software distribution

These script includes are installed with the Orchestration - Client Software Distribution plugin

<table id="table_g5x_fqc_ks"><thead><tr><th>

Script include

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CSDExtensionPoint

</td><td>

Execute the CSD provider’s specific code

</td></tr><tr><td>

CSDUtil

</td><td>

Utility functions for the CSD application.

</td></tr><tr><td>

RefQualsCSD

</td><td>

Reference qualifier filter. This script provides the filter functrions for the CSD providers, devices, SCCM application, install collections, and uninstall collections.

</td></tr><tr><td>

SCCMCatItemHandler

</td><td>

Sets the field values of specific SCCM catalog items. These values are the SCCM catalog item table name, catalog item name, SCCM provider, and SCCM software configuration.

</td></tr><tr><td>

SoftwareCatItemCreator

</td><td>

Creates software catalog items

</td></tr><tr><td>

CSDCatItemHandler

</td><td>

Base class for CSD catalog item creation. This script is used by the Create Catalog Item UI action to create and application catalog.

</td></tr><tr><td>

CSDDemoDataUtil

</td><td>

Populates demo data.

</td></tr><tr><td>

CSDDemoDataUtilAjax

</td><td>

Populates demo data.

</td></tr></tbody>
</table>## Properties installed with client software distribution

Properties for client software distribution \(CSD\) manage the installation status of requested software deployments and configure scheduled Discoveries.

To access CSD properties, navigate to **Client Software Distribution** &gt; **Properties**. The following properties are available:

<table id="table_lkm_djh_ms"><thead><tr><th>

Property

</th><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Status check expiration interval \(days\)

</td><td>

sn\_client\_sf\_dist.softwareInstallExpDays

</td><td>

Controls how many days the system waits before ignoring the software installation status. The default time limit for installing software is 30 days before the system stops checking the installation status of a deployment.Installation statuses are:

 -   **Not installed**: User has not installed requested software prior to the expiration of the configured time limit.
-   **Installed**: Software was installed within the configured time limit.
-   **Status check expired**: Time limit has expired for the user to install the requested software. The system no longer checks the status of this deployment.
-   **Revoked**: Software was [revoked](https://www.servicenow.com/docs/access?context=c_SCCMSoftwareRevocation&version=australia&pubname=australia-servicenow-platform&section=t_RevokeSoftwareInstalledFromSCCM&ft:locale=en-US) by the administrator.

 -   **Type**: integer
-   **Default value**: 30

</td></tr><tr><td>

Reconcile software installation status interval \(hours\)

</td><td>

sn\_client\_sf\_dist.softwareInstallIntervalHour

</td><td>

Determines when the scheduled job runs that determines the installation status. By default, the system checks the installation status every hour.-   **Type**: integer
-   **Default value**: 24

</td></tr><tr><td>

Set scheduled application Discovery interval \(days\).

</td><td>

sn\_client\_sf\_dist.discoveryExeDay

</td><td>

Sets the repeat interval for the scheduled job that runs application Discovery. By default, Discovery runs at midnight on the day set with this value. -   **Type**: integer
-   **Default value**: 5

</td></tr><tr><td>

Set lease execution schedule job interval \(minutes\)

</td><td>

sn\_client\_sf\_dist.lease\_execution\_interval

</td><td>

Interval in which the CSD Lease Schedule scheduled job checks for requested software leases to start, stop, or extend.-   **Type**: integer
-   **Default value**: 1

</td></tr><tr><td>

Set time prior to lease end to notify requester \(days\)

</td><td>

sn\_client\_sf\_dist.lease\_end\_notification

</td><td>

Determines how many days prior to the end of a software lease to notify the requester. If lease extensions are allowed, ensure that this period provides enough time for the approval process to complete before the lease expires.-   **Type**: integer
-   **Default value**: 5

</td></tr></tbody>
</table>## Workflows installed with client software distribution

These workflows are installed with the Orchestration - Client Software Distribution plugin

|Workflow|Description|
|--------|-----------|
|Discover SCCM|Retrieves lists of applications, collections, and deployments from SCCM servers using custom CSD orchestration activities. An administrator runs this workflow from a UI action in a [SCCM Server Instance record](../task/t_RetrieveSCCMDataClientSWDist.md#).|
|Order Client Software|Runs automatically when a user orders software from the service catalog.|
|Deploy SCCM Application|Triggered by the Order Client Software workflow to deploy software through SCCM server. This workflow adds either the user or the device into the SCCM collection.|
|Revoke Client Software|Begins the software revocation process for software deployed by an external provider. Administrators run this workflow from a UI action on the Requested Software record and the Installed Software Not Entitled record. This workflow triggers the appropriate provider workflow that performs the actual recovation. For example, this workflow triggers the Revoke SCCM Application workflow for applications in SCCM uninstall collections.|
|Revoke SCCM Application|Revokes SCCM applications that are members of an uninstall collection. The Revoke Client Software workflow triggers this workflow to revoke software deployed by an SCCM server. This workflow moves either the user or the device from the SCCM collection into the appropriate uninstall collection.|

**Related topics**  


[Using extension points to extend application functionality](https://www.servicenow.com/docs/access?context=extension-points&version=australia&pubname=australia-api-reference&ft:locale=en-US)

[Using scripted extension points in server-side scripts](https://www.servicenow.com/docs/access?context=scripted-extension-points&version=australia&pubname=australia-api-reference&ft:locale=en-US)

[Using UI extension points in server-side UI macros](https://www.servicenow.com/docs/access?context=ui-extension-points&version=australia&pubname=australia-api-reference&ft:locale=en-US)

[Using client extension points in client-side UI scripting](https://www.servicenow.com/docs/access?context=client-extension-points&version=australia&pubname=australia-api-reference&ft:locale=en-US)

