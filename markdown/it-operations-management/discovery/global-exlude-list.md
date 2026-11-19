---
title: Use Global Excludes List for IP addresses and ranges
description: Global Excludes List allows administrators to define global IP exclusions lists that work across Discovery schedules that discover configuration items, IP addresses, or networks. The list helps to prevent access to sensitive IPs as it blocks discovery when the IP is on the exclusion list. This feature is only applicable for Horizontal Discovery starting in the Rome release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/global-exlude-list.html
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Discovery IP address configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Use Global Excludes List for IP addresses and ranges

Global Excludes List allows administrators to define global IP exclusions lists that work across Discovery schedules that discover configuration items, IP addresses, or networks. The list helps to prevent access to sensitive IPs as it blocks discovery when the IP is on the exclusion list. This feature is only applicable for Horizontal Discovery starting in the Rome release.

## Before you begin

Global IP exclude ranges are active by default. To deactivate, uncheck the **Active** check box. This makes the records inactive and the entries aren't excluded from Discovery. You can add a single IP or an IP range to the Global Excludes list. The IP exclusion list \[ip\_exclusion\] table references existing IP collection tables and supports three types of collections: IP address list, IP address subnet, and IP address range.

**Note:** Use of Global Excludes List for IP addresses and ranges is not supported for IPv6 addresses. While the UI still allows users to add IPv6 addresses to the list, these addresses get ignored and are skipped from the exclusion process during Discovery.

Role required: discovery\_admin or agent\_admin role

## Procedure

1.  Navigate to **All** &gt; **Global IP Exclusion** &gt; **IP Exclusion**.

2.  Click **New** to create a new IP exclusion record.

3.  In the IP Excluded box, click the search icon to bring up the IP collections window.

4.  Select one of the IP collections listed or click **New** to bring up the IP Collections wizard.

5.  From the IP Collections wizard, select one of the three types of collections you want to create and fill in the necessary details.

    For each type, you can add a description on why you want to exclude particular IPs or which IPs are excluded.

    -   IP Address Range

        Fill in the details and then click **Submit**. This new range is added to the IP Exclusion list.

    -   IP Address Subnet

        Fill in the details and then click **Submit**. This new subnet is added to the IP Exclusion list.

    -   IP Address List

        Enter the name and then **Save**. The related list then shows at the bottom of the page. From the collections list, pick an existing item or click **New** to create a new list. Click **Update**. Remember the name you created. This new name is added to the collection list. Select this name from the list and click **Submit** again. This address list is added to the IP Exclusion list.

6.  Navigate to **Discovery** &gt; **Discovery Schedules** and select a schedule.

7.  If the schedule is for discovering configuration items, IP addresses, or networks, you can view the Global IP Exclusion tab at the bottom of the page.


## Result

When the scheduled Discovery runs, it skips the discovery of all IPs that are part of the active Global IP Exclusion record. All the rest of the IPs should be discovered.

**Note:** Overriding behavior is not applicable when the Discovery schedule has active Global IP exclusions.

If you try to run a Quick Discovery that includes an excluded IP, you will see an error message and Discovery will not be triggered.

