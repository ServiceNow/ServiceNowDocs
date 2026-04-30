---
title: Shazzam Insights dashboard
description: The Discovery Admin Workspace displays your port scanning information, IP address utilization, and Discovery schedules.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Discovery Admin Workspace Insights, Discovery Admin Workspace, Exploring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Shazzam Insights dashboard

The Discovery Admin Workspace displays your port scanning information, IP address utilization, and Discovery schedules.

![shazzam dashboard](../image/shazam_daw.png)

## Required ServiceNow AI Platform roles

-   discovery\_admin
-   admin

## Prerequisites

-   **Verify that you have the required setup**
    -   Discovery.
    -   Discovery Admin Workspace 1.3.1. \(August 2024 Store release\).
    -   CMDB Workspace
    -   Visibility Content
-   **Enable the data collection**

    Role required: system\_administrator.

    Set the **glide.discovery.shazzaminsights** property to **True**.

    Run a Discovery schedule. For more information, see: [Running discoveries in your network](running-discoveries.md).


## Access the Shazzam Insights dashboard

To open the dashboard, navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Insights** &gt; **Shazzam Insights**.

## Indicators

-   **Total IP addresses**

    The total number and the trend of IP address data that Shazzam scanned since a given date. The data is extracted from the Shazzam Summary \[shazzam\_summary\] table.

-   **Alive IP addresses**

    The number and the trend of responsive and pingable IP addresses that Shazzam scanned since a given date. The data is extracted from the Shazzam Status \[shazzam\_status\] table.

-   **Active IP addresses**

    The number and the trend of connected IP addresses that Shazzam scanned since a given date. The data is extracted from the Shazzam Status \[shazzam\_status\] table.

-   **Not reachable IPs**

    The number and the trend of unresponsive IP addresses that Shazzam scanned since a given date. The data is extracted from the Shazzam Summary \[shazzam\_summary\] table.

-   **Open ports**
    -   The score of SSH open ports
    -   The score of WMI open ports
    -   The score of WinRM SSL open ports
    -   The score of SNMP open ports
    -   The score of HTTP open ports
    -   The score of VmApp SSL open ports
    -   The score of SLP open ports

## Filters

<table id="table_llj_2vr_zbc"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

IP addresses

</td><td>

Boolean

</td><td>

The filter enables you to select all Discovery schedules you want to review by category. The available categories are:

-   IP Range
-   Alive
-   Active

</td></tr></tbody>
</table>