---
title: MID Server Upgrade History
description: Use this module to troubleshoot errors that occur during the MID Server upgrade process. The MID Server Upgrade Histories table contains a record of each instance upgrade. The MID Server Upgrade Stages table shows the status of each MID Server and its upgrade progress, including any errors encountered.
locale: en-US
release: zurich
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Resolving MID Server issues, MID Server reference, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server Upgrade History

Use this module to troubleshoot errors that occur during the MID Server upgrade process. The MID Server Upgrade Histories table contains a record of each instance upgrade. The MID Server Upgrade Stages table shows the status of each MID Server and its upgrade progress, including any errors encountered.

## MID Server Upgrade Histories

Users with admin or agent-admin roles can find detailed information for any MID Server upgrade in the Upgrade History module for MID Server. Whenever an instance is upgraded, all MID Servers in the Up state are upgraded automatically. The Upgrade History module uses the MID Server Upgrade Histories table \[ecc\_agent\_upgrade\_history\]. This table shows the following information:

-   The old instance version.
-   The new version.
-   The number of successfully upgraded MID Servers.
-   The number of MID Servers with pending upgrades. MID Servers have pending upgrades if the upgrade has failed or is in progress.

## MID Server Upgrade Stages

Select an instance record to see more details about the MID Servers upgraded with that instance. The Pending Upgrades and Complete Upgrade Details related lists use the MID Server Upgrade Stages table \[ecc\_agent\_upgrade\_history\_stage\]. MID Servers pinned to a specific version generate an entry with a blank MID Upgrade History on the MID Server Upgrade Stages table \[ecc\_agent\_upgrade\_history\_stage\].

<table id="table_llj_y3s_c3b"><tbody><tr><td>

MID Upgrade History

</td><td>

Refers to a corresponding record in the \[ecc\_agent\_upgrade\_history\] table.

</td></tr><tr><td>

Stage

</td><td>

Shows the progress of the MID Server through each stage of the upgrade process.

</td></tr><tr><td>

State

</td><td>

Shows the status of each stage.

</td></tr><tr><td>

Message

</td><td>

Displays dynamically generated messages about the upgrade stages, such as the file path to download directories or extract folders. It also displays information about any errors encountered, even if those errors do not block the upgrade.

</td></tr></tbody>
</table>**Parent Topic:**[Resolving MID Server issues](../reference/r_MIDServerTroubleshooting.md)

