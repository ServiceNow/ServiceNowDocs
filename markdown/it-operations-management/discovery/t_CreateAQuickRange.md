---
title: Create a Quick IP range for a Discovery schedule
description: Quick ranges enable administrators to define IP addresses to scan in a single comma-delimited string without creating separate records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/t\_CreateAQuickRange.html
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Discovery IP address configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Create a Quick IP range for a Discovery schedule

Quick ranges enable administrators to define IP addresses to scan in a single comma-delimited string without creating separate records.

## Before you begin

Only MID Servers that are up and validated are used with quick ranges. The MID Servers must specify the Discovery application \(or ALL applications\) and have IP ranges configured if you use the auto-select feature on the [Discovery schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/t_CreateADiscoverySchedule.md).

Role required: discovery\_admin

## About this task

You can enter IP addresses in one of the following formats:

-   An IP range defined by a slash and the number of bits in the subnetwork. For example, the string 10.10.10.0/24 scans 24 bits of IP addresses from 10.10.10.0 to 10.10.10.254.
-   An IP range defined by a dash. For example, the string 10.10.11.0-10.10.11.165 scans the IP addresses from 10.10.11.0 to 10.10.11.165.
-   A comma-separated list of specific IP addresses. For example, the string 10.0.2.1,10.0.2.15 scans the IP addresses 10.0.2.1 and 110.0.2.15.

**Note:** IPv6 address ranges and networks aren't supported and will be ignored. Any other entries that can't be interpreted will also be ignored.

## Procedure

1.  Select the **Quick Ranges** related link on the Discovery Schedule form.

2.  Enter the IP ranges and specific IP addresses to scan.

3.  Select **Make Ranges**.

    **Note:** The Quick Range interface is for entering IP addresses only and can't be used to edit IP addresses that have already been submitted.

    \[Omitted image "DiscoveryQuickRanges.png"\] Alt text: Entering a quick range

    The instance automatically displays the entries in the proper format.

4.  For changes to IP address ranges, select the IP address records in the **Discovery Range Sets** related list.

    **Note:** Overriding behavior is not applicable on Discovery range sets.


