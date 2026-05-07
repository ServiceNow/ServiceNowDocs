---
title: Activate auto-created Discovery schedules
description: Activate schedules that were created automatically via the Discovery and IP Address Management \(IPAM\) integration.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 3
breadcrumb: [IPAM Discovery integration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Activate auto-created Discovery schedules

Activate schedules that were created automatically via the Discovery and IP Address Management \(IPAM\) integration.

## Before you begin

Confirm the following:

-   You have at least one validated MID Server with a status of **Up**. The MID Server must reach the IP ranges that you intend to discover. You can install the MID Server by using [Use MID Server guided setup](https://www.servicenow.com/docs/access?context=use-mid-server-guidedsetup&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) or by manually downloading and running the installer. For details, see the MID Server installation instructions for [Linux](https://www.servicenow.com/docs/access?context=t_InstallAMIDServerOnLinux&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) and [Windows](https://www.servicenow.com/docs/access?context=mid-server-install-prereqs&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).
-   You have installed and configured Service Graph Connector Central \(SGC Central\) v2.4.0. For more information, see [Configuring SGC Central](https://www.servicenow.com/docs/access?context=sgcc-configuring&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).
-   You have installed and configured Service Graph Connector for Infoblox v1.5.0. For more information, see [Configure Service Graph Connector for Infoblox using SGC Central](https://www.servicenow.com/docs/access?context=sgcc-configure-infoblox-integ&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).
-   You have enabled auto-created schedules in [Discovery Admin Workspace Settings](../concept/discovery-admin-workspace-setup.md). For more information, see [Configure auto-created Discovery schedules](config-auto-disco-schedules.md).
-   You're using Discovery Admin Workspace v1.15.0.
-   You're using the Australia, ZP8 or later, or YP13 or later version of the ServiceNow AI Platform.

Role required: discovery\_admin

## About this task

The IPAM to Discovery integration monitors your IPv6 network structure by tracking changes in managed networks, subnets, and IP addresses. Automatic schedule creation uses your network topology to generate Discovery schedules and organizes them by location when location data is available. Auto-created schedules are inactive by default and must be manually activated before they can run.

## Procedure

1.  Navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Schedules** &gt; **IP-based discovery**.

2.  Select **View and activate schedules** from the **Needs attention** section.

3.  Select the check box next to the name of the auto-created schedule that you want to activate.

    Alternatively, you can activate all the schedules by selecting the check box next to the **Name** column.

4.  Select **Activate**.

    An Activate schedule? dialog displays.

5.  Select the **MID Server** drop-down list and choose a MID Server selection method.

    |Option|Description|
    |------|-----------|
    |**Specific MID Server**|Select this option to search for an existing MID Server. Only MID Servers that are validated and up display in the search results.|
    |**Specific MID Cluster**|Select this option to search for an existing MID Server cluster. Clusters provide failover protection and load balancing between MID Servers. See [Configure a MID Server cluster](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) for more information.|

6.  Select the **Run settings** drop-down list and configure when the schedule will run.

    |Option|Description|
    |------|-----------|
    |**On Demand**|The schedule only runs when triggered manually.|
    |**After Discovery**|The schedule runs after a specified Discovery schedule completes.|
    |**Weekly**|The schedule runs weekly on a specified day, or days, and time.|
    |**Monthly**|The schedule runs once a month on a specified day and time.|
    |**Periodically**|The schedule runs at a specified repeat interval, such as every number of days, hours, or minutes.|
    |**Once**|The schedule runs one time only on a specified date and time.|
    |**Daily**|The schedules runs once a day at a specified time.|
    |**Calendar Quarter End**|The schedule runs on the last day of each quarter at a specified time.|

7.  Set a time limit for running this schedule.

    When the configured time elapses, the remaining tasks for the discovery are canceled, even if the scan isn’t complete. Use this field to limit system load to a desirable time window. If no value is entered in this field, this schedule runs until complete. If the schedule exceeds the maximum runtime, it's canceled.

8.  Select **Save and activate**.

    The system automatically runs the synchronization job according to your schedule, keeping your discovery targets updated with the latest IPv6 information from IPAM.


**Related topics**  


[IPAM Discovery integration](../concept/ipv6-ipam-disco-integration.md)

