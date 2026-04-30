---
title: Run a Quick Discovery
description: Quick Discovery, or DiscoverNow, allows an administrator to run a CI Configuration discovery on a single IP address without requiring a schedule.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Schedule a horizontal discovery, Running discoveries in your network, Discovery, ITOM Visibility, IT Operations Management]
---

# Run a Quick Discovery

Quick Discovery, or DiscoverNow, allows an administrator to run a CI Configuration discovery on a single IP address without requiring a schedule.

## Before you begin

Role required: discovery\_admin

## About this task

The platform automatically selects the correct MID Server to use for the discovery if one is associated with the IP address selected. If no MID Server is configured for the network in which that address appears, you can select a MID Server. Use this feature to discover new devices in the network as soon as they are connected to the network, rather than waiting for a regularly scheduled discovery.

To configure the system to automatically determine which MID Server to use, set up the IP range capabilities for each MID Server in your system.

You can run DiscoverNow from a Discovery schedule form or from a script.

**Note:** Quick Discovery using a IPv6 target address is supported.

## Procedure

1.  Open Quick Discovery from one of these locations:

    -   Navigate to **Discovery** &gt; **Discovery Schedules** and click **Quick Discovery** in the header bar.
    -   Navigate to **Discovery** &gt; **Home** and click **Discovery Quick Start** under the Schedules tile.
    A dialog box appears asking for an IP address and the name of the MID Server to use. Only **Up** and **Validated** MID Servers are available.

2.  Enter the target IP address for a discovery in the **Target IP** field.

    **Note:** DiscoverNow does not currently support IP network discovery. Make sure that you enter a single IP address only and not an entire network, such as 10.105.37.0/24.

    When a MID Server is assigned to the subnet containing the target IP address and currently in an operational status of **Up**, the name appears automatically in the **MID Server** field. If multiple MID servers are found, the system selects one for you. The value in the **MID Server** field can be overwritten if you want to select a different MID Server.

    **Important:** If the selected MID Server is part of a load balanced cluster and becomes unavailable for any reason, the instance does not assign another MID Server from that cluster to the quick Discovery. You must select another MID Server from the list of appropriate MID Servers.

3.  If no MID Server is defined for that network, select one from the list of available MID Servers.

    ![Quick discovery](../image/QuickDiscoveryDialog.png "Quick Discovery Dialog")

4.  Click **OK** to run discovery.

    The status record for that discovery appears. The **Schedule** column is empty because no schedule is associated with this discovery.

    ![Quick discovery status list](../image/QuickDiscoveryStatusList.png "Quick Discovery Status List")


