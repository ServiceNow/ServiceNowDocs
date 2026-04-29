---
title: Properties installed
description: Properties for client software distribution \(CSD\) manage the installation status of requested software deployments and configure scheduled Discoveries.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Components installed with CSD, Client Software Distribution, Integration Hub solutions, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Properties installed

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
-   **Revoked**: Software was [revoked](../tasks/revoke-from-serv-cat.md) by the administrator.

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
</table>**Parent Topic:**[Components installed with client software distribution](comp-installed-csd-ihub.md)

