---
title: Configure auto-created Discovery schedules
description: Enable the system to automatically create Discovery schedules based on IP data from your IP Address Management \(IPAM\) connections.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 2
breadcrumb: [IPAM Discovery integration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Configure auto-created Discovery schedules

Enable the system to automatically create Discovery schedules based on IP data from your IP Address Management \(IPAM\) connections.

## Before you begin

Confirm the following:

-   You have installed and configured Service Graph Connector Central \(SGC Central\) v2.4.0. For more information, see [Configuring SGC Central](https://www.servicenow.com/docs/access?context=sgcc-configuring&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
-   You have installed and configured Service Graph Connector for Infoblox v1.5.0. For more information, see [Configure Service Graph Connector for Infoblox using SGC Central](https://www.servicenow.com/docs/access?context=sgcc-configure-infoblox-integ&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
-   You're using Discovery Admin Workspace v1.13.0.
-   You're using the Zurich, ZP9 or later, or YP13 or later version of the ServiceNow AI Platform.

Role required: discovery\_admin

## About this task

The IPAM to Discovery integration monitors your IPv6 network structure by tracking changes in managed networks, subnets, and IP addresses. Automatic schedule creation uses your network topology to generate Discovery schedules and organizes them by location when location data is available. Additional checks maintain the appropriate schedule size by evaluating the number of IP addresses in each schedule and updating them when IPs are added, removed, or deactivated.

## Procedure

1.  Navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Settings** &gt; **IP Address Management \(IPAM\)**.

2.  Select the **Enable auto-created schedules** toggle.

3.  Enter a tag key to determine how IPs are assigned to schedules.

    Discovery evaluates the key that you provide, retrieves the corresponding value from your IPAM data by looking it up in the Key Values \[cmdb\_key\_value\] table, where it searches only subnet records. IPs that share values are assigned to the same schedule, allowing the schedule structure to follow meaningful attributes such as location or environment.

    **Note:** You can enter a single space in the **Tag key** field if you don't want to provide a key.

4.  Configure when the automatic synchronization job runs.

    1.  Select a frequency from the **Update frequency** drop-down list.

    2.  Enter the time of day that you want the IP data to refresh.

    3.  Choose a start date.

5.  Select **Save**.

    The system automatically runs the synchronization job according to your schedule, keeping your discovery targets updated with the latest IPv6 information from IPAM.

6.  To synchronize your IP data immediately instead of waiting for the next refresh time, select **Refresh IP data**.


## What to do next

After you enable auto-created schedules and configure the IP data refresh settings, IPAM generates a corresponding Discovery schedule. The schedule is inactive when it's created, so make sure to activate it before it runs. For more information, see [Activate auto-created Discovery schedules](activate-auto-disco-schedule.md).

**Related topics**  


[IPAM Discovery integration](../concept/ipv6-ipam-disco-integration.md)

