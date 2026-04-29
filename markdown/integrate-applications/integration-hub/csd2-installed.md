---
title: Components installed with CSD 2.0
description: Several types of components are installed with the CSD 2.0 application.These tables are installed with the Client Software Distribution 2.0 application plugin \(com.sn.csd\).These roles are installed with the CSD 2.0 application.Properties for CSD 2.0 manage the installation status of requested software deployments and configure scheduled Discoveries.These flows, subflows, and actions are with the CSD 2.0 application.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Client Software Distribution 2.0 application, Integration Hub solutions, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Components installed with CSD 2.0

Several types of components are installed with the CSD 2.0 application.

**Parent Topic:**[Client Software Distribution 2.0 application](../concept/csd-app-2.md)

## Tables installed

These tables are installed with the Client Software Distribution 2.0 application plugin \(com.sn.csd\).

|Table|Description|
|-----|-----------|
|Client Software Distribution Provider \[sn\_csd\_provider\]|Contains all software distribution providers.|
|CSD Catalog Item Fulfillment Configuration \[sn\_csd\_cat\_item\_fulfilment\_config\]|Contains additional configuration information required for ordering a catalog item using CSD 2.0.|
|Client Software Distribution Software Configuration \[sn\_csd\_software\_config\]|Base table for all software provider configurations.|
|Client Software Distribution Lease Execution \[sn\_csd\_lease\_execution\]|Contains scripts that are scheduled to run the subflows and flows associated with deployment, revocation, and lease management.|
|Device Entitlement \[sn\_csd\_entitlement\_asset\]|Contains information about the license allocation for devices.|
|Client Software Distribution Application \[sn\_csd\_application\]|Base table for all software provider applications.|
|Client Software Distribution Lease Manager \[sn\_csd\_lease\_manager\]|Links the requested item with the required lease execution and schedule.|
|User Entitlement \[sn\_csd\_entitlement\_user\]|Contains information about the license allocation for users.|
|License Entitlement \[sn\_csd\_entitlement\]|Parent table for the device and user entitlement tables.|
|Client Software Distribution Lease Schedule \[sn\_csd\_lease\_schedule\]|Contains the schedule entries for deployment, lease and revocation.|
|Software Entitlement \[sn\_csd\_license\]|Contains licensing information of the required software model.|
|Software Model \[sn\_csd\_software\_product\_model\]|Contains details of the required software. The. details include display name, manufacturer, and so on.|
|Requested Software \[sn\_csd\_req\_software\]|Contains all requested software, and their statuses.|

## Roles installed

These roles are installed with the CSD 2.0 application.

<table id="table_h8t_4dc_kg"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CSD Admin\[sn\_csd.CSD Admin\]

</td><td>

Administrator role for managing CSD 2.0.

</td></tr><tr><td>

CSD User \[sn\_csd.CSD User\]

</td><td>

Role to order catalog items from the catalog using CSD 2.0 and to perform actions such as revoke software, extend lease, and so on.

</td></tr></tbody>
</table>## Properties installed

Properties for CSD 2.0 manage the installation status of requested software deployments and configure scheduled Discoveries.

To access CSD 2.0 properties, navigate to **Client Software Distribution 2.0** &gt; **Properties**. The following properties are available:

<table id="table_l3m_gj3_ms"><thead><tr><th>

Property

</th><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Status check expiration interval \(days\). Configure the number of days the system should wait before ignoring the software installation status.

</td><td>

sn\_csd.softwareInstallExpDay

</td><td>

Controls how many days the system waits before ignoring the software installation status. The default time limit for installing software is 30 days before the system stops checking the installation status of a deployment.-   **Type**: integer
-   **Default value**: 30

 Installation statuses are:

 -   **Not installed**: User has not installed requested software prior to the expiration of the configured time limit.
-   **Installed**: Software was installed within the configured time limit.
-   **Status check expired**: Time limit has expired for the user to install the requested software. The system no longer checks the status of this deployment.
-   **Revoked**: Software was revoked by the administrator.
-   **Not Synced**: Installation status is not synchronized with the status in the server.

 **Note:** If SAM is used along with CSD 2.0, the status is updated automatically. Else, the admin should change the status manually.

</td></tr><tr><td>

Reconcile software installation status interval \(hours\). Set the repeat interval for the scheduled job that determines the installation status.

</td><td>

sn\_csd.softwareInstallIntervalHour

</td><td>

Determines when the scheduled job runs that determines the installation status. By default, the system checks the installation status every hour.-   **Type**: integer
-   **Default value**: 24

</td></tr><tr><td>

Set scheduled application Discovery interval \(days\).

</td><td>

sn\_csd.discoveryExeDay

</td><td>

Sets the repeat interval for the scheduled job that runs application Discovery. By default, Discovery runs at midnight on the day set with this value. -   **Type**: integer
-   **Default value**: 5

</td></tr><tr><td>

Set lease execution schedule job interval \(minutes\)

</td><td>

sn\_csd.lease\_execution\_interval

</td><td>

Interval in which the CSD Lease Schedule scheduled job checks for requested software leases to start, stop, or extend.-   **Type**: integer
-   **Default value**: 1

</td></tr><tr><td>

Set time prior to lease end to notify requester \(days\).

</td><td>

sn\_csd.lease\_end\_notification

</td><td>

Determines how many days prior to the end of a software lease to notify the requester. If lease extensions are allowed, ensure that this period provides enough time for the approval process to complete before the lease expires.-   **Type**: integer
-   **Default value**: 5

</td></tr><tr><td>

Determines whether to use SAM plugin\(SAM Foundation or SAM Professional\) tables for managing software models and licensing information

</td><td>

sn\_csd.useSAMPlugin

</td><td>

Option to use SAM plugin along with CSD 2.0 and choose SAM tables.

</td></tr></tbody>
</table>## Flows, subflows, and actions

These flows, subflows, and actions are with the CSD 2.0 application.

|Flow| |
|----|---|
|Order Client Software|Schedules the installation of an ordered application on the selected device. The request requires approvals based on the user input in the catalog item configuration.|
|Deploy Client Software|Deploys a software by executing provider-specific subflow. Creates catalog tasks if there is a failure in the execution of the provider subflow.|

|Subflow|Description|
|-------|-----------|
|Assign License|Creates an entitlement record.|
|Client Software Lease Extend|Extends the lease end date of the required software.|
|CSD Deploy Software Post Processing|Performs post processing after the software deployment is successful.|
|CSD Lease End Notification|Notifies user about the lease end date of the software and send link to extend lease end date.|
|Delete Lease Records|Deletes the lease schedule, lease execution, and lease manager records associated with the requested item.|
|Deploy Application Template|Flow template for the Deploy Application flow.|
|Look up Configuration Data Template|Flow template for the Look up Configuration Data flow.|
|Revoke Application Template|Flow template for the Revoke Application flow.|
|Revoke License|Removes the specified entitlement record.|
|Revoke Client Software|Revokes software from the provider server.|
|Look Up Applications|Returns the list of application details found for each software provider.|
|Look up SAM Software Models|Returns the list of SAM software models related to the specified application.|
|Configure SAM Software Model|Configures the SAM software model of the specified application.|
|Configure CSD Software Model|Configures the CSD software model of the specified application.|

|Action|Description|
|------|-----------|
|Get CSD Record URL|Generates link for the requested software.|
|Is Date Empty|Verifies if the input date is empty.|
|License Validation|Checks the license availability and retrieves the license information if available.|
|Update Lease End on Requested Item|Updates the lease end date of the requested item record.|

