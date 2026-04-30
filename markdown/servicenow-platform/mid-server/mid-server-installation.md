---
title: Installing the MID Server
description: Download and install the MID Server on the host machine, test the connection, and then validate the MID Server. Use the manual procedures or the guided setup. Set up multiple MID Servers for load balancing and domain separation. These procedures prepare it for use with any application.
locale: en-US
release: xanadu
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Installing the MID Server

Download and install the MID Server on the host machine, test the connection, and then validate the MID Server. Use the manual procedures or the guided setup. Set up multiple MID Servers for load balancing and domain separation. These procedures prepare it for use with any application.

<table id="table_ngw_1v4_nhb"><tbody><tr><td>

![Set up indicator for installation phase](../image/ProgressBarInstall.png)

</td></tr></tbody>
</table>Prerequisites: Ensure the [MID Server system requirements](../reference/r_MIDServerSystemRequirements.md) and [MID Server connection prerequisites](c_MIDServerConnectionPrerequisites.md#) are met before you install the MID Server manually or use the guided setup utility.

## MID Server manual installation

The manual process requires these setup tasks, performed in the order shown here:

1.  [Create the MID Server user account](../task/t_SetupMIDServerRole.md#) and grant the appropriate role to this user.
2.  [Download the installer file](../task/t_DownloadMIDServerFiles.md) for the host machine.
3.  Install the MID Server on a [Linux](../task/t_InstallAMIDServerOnLinux.md#) or [Windows](mid-server-install-prereqs.md#) host.
4.  [Validate the MID Server](../task/t_ValidateAMIDServer.md) to ensure that it is trusted to access credentials used by the instance for automations.
5.  [Test connectivity](../task/t_ValidateNetworkConnectivity.md) between the MID Server and the instance for automatic upgrades.
6.  Optionally, [deploy multiple MID Servers](../task/t_InstallMultplMIDSvrOnASingleSys.md#) in your network for load balancing or when domain separation is enabled.

## MID Server guided setup

Alternatively, the [MID Server Guided Setup](../task/use-mid-server-guidedsetup.md) streamlines the process and allows you to set up a basic MID Server quickly.

