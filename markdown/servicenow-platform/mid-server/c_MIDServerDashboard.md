---
title: MID Server dashboard
description: The MID Server dashboard is a central place for MID Server users to monitor ongoing operations. The dashboard consists of reports and gauges that display information from the MID Server Status table.
locale: en-US
release: yokohama
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 10
breadcrumb: [MID Server reference, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server dashboard

The MID Server dashboard is a central place for MID Server users to monitor ongoing operations. The dashboard consists of reports and gauges that display information from the MID Server Status table.

<table id="table_jmp_fsf_khb"><tbody><tr><td>

![Links to each of the MID Server sections](../image/MIDRefIconBar.png)

</td></tr></tbody>
</table>The MID Server Dashboard is available from the **MID Server** &gt; **Dashboard** module.

After upgrading to Discovery Admin Workspace version 1.3.1 \(August 2024 Store\), you can navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Insights** and use the enhanced dashboard.

## MID Server Overview tab

The Overview tab provides graphs showing the status of MID Servers, including any validation issues or pending upgrades and jobs. The tab also displays which MID Servers by capability.

![MID Server overview tab.](../image/mid-dashboard-overview.png)

## MID Server Performance tab

The Performance tab displays information relating to the MID Server CPU and memory usage, including the life-cycle event history.

![Performance tab layout.](../image/mid-dashboard-performance.png)

## MID Server Custom performance tab

The Custom performance tab enables users to set custom MID Server selection criteria to show particular MID Servers in a select time frame.

![Custom performance tab.](../image/mid-dashboard-custom.png)

## MID Server status gauge

The MID Server Status gauge on the dashboard displays basic information about each MID Server. This information comes from the MID Server Status \[ecc\_agent\_status\] table.

![The MID Server Dashboard gauge](../image/MidServerDashbardGauge.png "MID Server Dashboard gauge")

If the version is not compatible, the MID Server status is not changed to **Down** in the MID Server dashboard. So it might still appear to be processing commands when it actually is not doing so. You must check the MID Server **Version** on the dashboard.

See [KB0535181](https://support.servicenow.com/kb_view.do?sysparm_article=KB0535181) for additional MID Server troubleshooting information.

The icons in the **Version** column indicates the following:

-   **Red**: Incompatible. The MID Server and instance do not belong to the same release. You must [upgrade the MID Server](../task/t_UpgradeTheMIDServerManually.md) and verify that it is not pinned to an older version with the [mid.version.override](../reference/mid-server-version-selection.md) property. The MID Server will not be upgraded until the parameter is cleared.
-   **Yellow**: Compatible, but an upgrade is recommended. This indicates that the MID Server version belongs to the same family as the instance, but not the same version.
-   **Green**: Compatible. No upgrade necessary.
-   **Gray**: Incompatible. The instance cannot detect the version.

<table id="table_ucv_ytv_xv"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the MID Server.

</td></tr><tr><td>

Host name

</td><td>

The name of the system that hosts the MID Server.

</td></tr><tr><td>

Status

</td><td>

The status of the MID Server.

</td></tr><tr><td>

Validated

</td><td>

Whether or not the MID Server was [validated](../task/t_ValidateAMIDServer.md).

</td></tr><tr><td>

Max memory used %

</td><td>

The highest percent usage of memory on the system that hosts the MID Server, in the configured sampling interval. The default interval is 30 minutes, but this value is user configurable. See [MID Server resource threshold alerts](../reference/mid-resource-threshold-alerts.md) for details.

</td></tr><tr><td>

Mean CPU used %

</td><td>

The average percent usage of CPU on the system that hosts the MID Server, in the configured sampling interval. The default interval is 30 minutes, but this value is user configurable. See [MID Server resource threshold alerts](../reference/mid-resource-threshold-alerts.md) for details.

</td></tr><tr><td>

Pending jobs

</td><td>

Number of pending ECC queue jobs for that MID Server.

</td></tr><tr><td>

Processing jobs

</td><td>

Number of processing ECC queue jobs for that MID Server.

</td></tr><tr><td>

Version

</td><td>

The version of the MID Server. An icon indicates the validity of the MID Server:-   **Red**: Incompatible. The MID Server and instance do not belong to the same release. You must [upgrade the MID Server](../task/t_UpgradeTheMIDServerManually.md) and verify that it is not pinned to an older version with the [mid.version.override](../reference/mid-server-version-selection.md) property. The MID Server will not be upgraded until the parameter is cleared.
-   **Yellow**: Compatible, but an upgrade is recommended. This indicates that the MID Server version belongs to the same family as the instance, but not the same version.
-   **Green**: Compatible. No upgrade necessary.
-   **Gray**: Incompatible. The instance cannot detect the version.

</td></tr><tr><td>

User

</td><td>

The login name of the user. An icon indicates the validity of the user:-   **Red**: Incompatible. The user does not have the[mid\_server role](../task/t_SetupMIDServerRole.md#) or the user does not match the value in the [mid.instance.username parameter](../task/t_SetupMIDServerRole.md#) \(in the `config.xml` configuration file\). Reconfigure the MID Server user and [verify that it works](../task/t_SetupMIDServerRole.md#).
-   **Green**: Compatible. The user has the mid\_server role and matches the user in the configuration file.

 **Note:** The user can also have any of the SOAP roles that the [mid\_server role](../task/t_SetupMIDServerRole.md#) inherits.

</td></tr></tbody>
</table>**Parent Topic:**[MID Server reference](mid-server-reference-information.md)

**Related topics**  


[MID Server system requirements](../reference/r_MIDServerSystemRequirements.md)

[MID Server upgrades](c_UpgradeAndTestMIDServer.md)

[Resolving MID Server issues](../reference/r_MIDServerTroubleshooting.md)

[MID Server properties](../reference/r_MIDServerProperties.md#)

[MID Server parameters](../reference/mid-server-parameters.md#)

[MID Server Configuration Parameter settings and priority](../reference/mid-config-param-priority.md)

[MID Server File Cleaner](mid_file_cleaner.md)

[MID Server protected records and reserved characters](../reference/mid-server-reserved-characters.md)

[MID Server privileged commands](c_PrivilegedCommandsForMIDServer.md#)

[MIDSystem methods](../reference/r_MIDSystemMethods.md)

[Manually start, stop, and restart a MID Server](../task/t_InstallMIDServerAsWinService.md)

[MID Server heartbeat](../reference/r_MIDServerHeartbeat.md)

[Set the MID Server JVM memory size](../task/t_MIDServerOptionalConfiguration.md)

[Pause the MID Server](../task/t_PauseTheMIDServer.md#)

