---
title: Activate auto-created Discovery schedules
description: Activate schedules that were created automatically via the Discovery and IP Address Management \(IPAM\) integration.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 4
breadcrumb: [IPAM Discovery integration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Activate auto-created Discovery schedules

Activate schedules that were created automatically via the Discovery and IP Address Management \(IPAM\) integration.

## Before you begin

Confirm the following:

-   You have at least one validated MID Server with a status of **Up**. The MID Server must reach the IP ranges that you intend to discover. You can install the MID Server by using [Use MID Server guided setup](https://www.servicenow.com/docs/access?context=use-mid-server-guidedsetup&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) or by manually downloading and running the installer. For details, see the MID Server installation instructions for [Linux](https://www.servicenow.com/docs/access?context=t_InstallAMIDServerOnLinux&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) and [Windows](https://www.servicenow.com/docs/access?context=mid-server-install-prereqs&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).
-   You have installed and configured Service Graph Connector Central \(SGC Central\) v2.4.0. For more information, see [Configuring SGC Central](https://www.servicenow.com/docs/access?context=sgcc-configuring&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).
-   You have installed and configured Service Graph Connector for Infoblox v1.5.0. For more information, see [Configure Service Graph Connector for Infoblox using SGC Central](https://www.servicenow.com/docs/access?context=sgcc-configure-infoblox-integ&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).
-   You have enabled auto-created schedules in [Discovery Admin Workspace Settings](../concept/discovery-admin-workspace-setup.md). For more information, see [Configure auto-created Discovery schedules](config-auto-disco-schedules.md).
-   You're using Discovery Admin Workspace v1.13.0.
-   You're using the Yokohama, ZP9 or later, or YP13 or later version of the ServiceNow AI Platform.

Role required: discovery\_admin

## About this task

The IPAM to Discovery integration monitors your IPv6 network structure by tracking changes in managed networks, subnets, and IP addresses. Automatic schedule creation uses your network topology to generate Discovery schedules and organizes them by location when location data is available. Auto-created schedules are inactive by default and must be manually activated before they can run.

## Procedure

1.  Navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Schedules** &gt; **IP-based discovery**.

2.  Select **View and activate schedules** from the **Needs attention** section.

3.  Select the check next to the name of the auto-created schedule that you want to activate.

    Alternatively, you can activate all the schedules by selecting the check next to the **Name** column.

4.  Select **Activate**.

    An Activate schedule? dialog displays.

5.  Select the **MID Server** drop-down list and choose a MID Server selection method.

    |Option|Description|
    |------|-----------|
    |**Specific MID Server**|Select this option to search for an existing MID Server. Only MID Servers that are validated and up display in the search results.|
    |**Specific MID Cluster**|Select this option to search for an existing MID Server cluster. Clusters provide failover protection and load balancing between MID Servers. See [Configure a MID Server cluster](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) for more information.|

6.  Select the **Run settings** drop-down list and configure when the schedule will run.

    **Important:** Until an auto-created schedule is activated, only the **On Demand** option is supported. Additional run settings are visible in the **Run settings** drop-down list but aren't functional in this release. After you activate the schedule, you can configure run settings in the [Schedule details](../concept/c_daw-disco-schedule-details.md) form or via the Discovery Schedules \[discovery\_schedule\] table. Additional details are provided below.

<table id="choicetable_brn_q3y_j3c"><thead><tr><th align="left" id="d223510e305">

Option

</th><th align="left" id="d223510e308">

Description

</th></tr></thead><tbody><tr><td id="d223510e314">

**On Demand**

</td><td>

The schedule only runs when triggered manually.

</td></tr><tr><td id="d223510e323">

**After Discovery**

</td><td>

The schedule runs after a specified Discovery schedule completes.**Important:** This option must be configured post activation in the [Schedule details](../concept/c_daw-disco-schedule-details.md) form.

</td></tr><tr><td id="d223510e346">

**Weekly**

</td><td>

The schedule runs once a week on a specified day and time.**Note:** By default, the auto-created schedule runs on the first day of the week. To specify a different day, activate the schedule and then configure the run settings in the [Schedule details](../concept/c_daw-disco-schedule-details.md) form.

</td></tr><tr><td id="d223510e369">

**Weekdays**

</td><td>

The schedule runs Monday through Friday at a specified time.

</td></tr><tr><td id="d223510e379">

**Monthly**

</td><td>

The schedule runs once a month on a specified day and time.**Note:** By default, the auto-created schedule runs on the first day of the week. To specify a different day, activate the schedule and then configure the run settings in the [Schedule details](../concept/c_daw-disco-schedule-details.md) form or via the Discovery Schedules \[discovery\_schedule\] table.

</td></tr><tr><td id="d223510e402">

**Periodically**

</td><td>

The schedule runs at a specified repeat interval, such as every number of days, hours, or minutes.**Important:** This option must be configured post activation in the [Schedule details](../concept/c_daw-disco-schedule-details.md) form.

</td></tr><tr><td id="d223510e425">

**Weekends**

</td><td>

The schedule runs on Saturday and Sunday at a specified time.

</td></tr><tr><td id="d223510e434">

**Once**

</td><td>

The schedule runs one time only on a specified date and time.**Important:** This option must be configured post activation in the [Schedule details](../concept/c_daw-disco-schedule-details.md) form.

</td></tr><tr><td id="d223510e457">

**Month Last Day**

</td><td>

The schedule runs on the last day of each month at a specified time.

</td></tr></tbody>
</table>7.  Set a time limit for running this schedule.

    When the configured time elapses, the remaining tasks for the discovery are canceled, even if the scan isn’t complete. Use this field to limit system load to a desirable time window. If no value is entered in this field, this schedule runs until complete. If the schedule exceeds the maximum runtime, it's canceled.

8.  Select **Save and activate**.

    The system automatically runs the synchronization job according to your schedule, keeping your discovery targets updated with the latest IPv6 information from IPAM.


**Related topics**  


[IPAM Discovery integration](../concept/ipv6-ipam-disco-integration.md)

