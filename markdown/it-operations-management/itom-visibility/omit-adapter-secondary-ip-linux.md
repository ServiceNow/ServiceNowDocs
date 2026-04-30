---
title: Omit network adapter secondary IP addresses in Linux discovery
description: Limit Linux discovery to specific network adapters and their primary IP addresses to improve performance by ignoring secondary IP addresses.
locale: en-US
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Linux, Operating systems discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Omit network adapter secondary IP addresses in Linux discovery

Limit Linux discovery to specific network adapters and their primary IP addresses to improve performance by ignoring secondary IP addresses.

## About this task

Configuring the **network\_adapter\_exclusion\_list** system property ensures that only specified network adapters and their primary IP addresses are used during Linux discovery. Secondary IP addresses that are not named are automatically omitted.

## Before you begin

Role required: admin

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  In the **Name** field, search for `network_adapter_exclusion_list`.

3.  Select the **network\_adapter\_exclusion\_list** property.

4.  In the **Value** field, enter the network adapter associated with the NIC IP address to exclude it from deletion.

    The network adapter must be entered in one of the formats listed in the following table.

    |Format|Description|
    |------|-----------|
    |Single name|Single adapter name. For example: `bond0`.|
    |Regular expression matching multiple adapter names|Regular expression that matches multiple adapter names ending with one or more digits. For example: `bond\d+`.|
    |Multiple adapter names|Multiple adapter names, separated by commas, including regular expression. For example: `nic1,bond\d+`.|

5.  Select **Update**.


## Result

When the predefined schedule triggers the Linux server discovery or a scheduled horizontal discovery runs, only the specific network adapters and their primary IP addresses are included in the discovery process.

For more information, see [Schedule a horizontal discovery](../../discovery/task/t_CreateADiscoverySchedule.md#).

**Related topics**  


[Linux discovery](../../discovery/reference/r_DataCollDiscoLinuxComputers.md)

