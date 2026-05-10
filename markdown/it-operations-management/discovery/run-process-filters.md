---
title: Running process filters
description: Filter any processes, using combinations of name and key parameters, from coming back to the instance. Out-of-the box, you can filter OS processes. Filtering processes helps reduce the number of records created, updated, or deleted in the database which can improve overall database performance.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Advanced Discovery configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Running process filters

Filter any processes, using combinations of name and key parameters, from coming back to the instance. Out-of-the box, you can filter OS processes. Filtering processes helps reduce the number of records created, updated, or deleted in the database which can improve overall database performance.

## Before you begin

Role required: discovery\_admin or admin

## About this task

To add processes to the filter, you must setup configurations using the Running Process filter record \[running\_process\_filter\]. These records make sure the filtered processes do not populate the Running process \[cmdb\_running\_process\] table.

## Procedure

1.  Navigate to running\_process\_filter.list.

2.  Select **New** to create a record.

    The form and descriptions are explained below.

    ![Running process filters form](../image/running_process_filter_record.png)

<table id="table_rxm_mty_rxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Check the box to include or exclude.

</td></tr><tr><td>

Name

</td><td>

Name for the record.

</td></tr><tr><td>

Description

</td><td>

Short description of the record.

</td></tr><tr><td>

Category

</td><td>

A name for the configuration type. Running process filters can be grouped however you want so that it's easier to identify and choose in the table.

</td></tr><tr><td>

Probe

</td><td>

Mandatory field. Which probe will use this filter. Often Linux or Windows active processes or ADM enhanced. When the probe executes, the instance sends the running\_process\_filter records as a probe parameter. The probe then uses this to filter the results before sending the information back to the instance.

</td></tr><tr><td>

Discovery Schedule

</td><td>

You can apply the filter on a specific Discovery schedule. If you leave this field, it applies to all schedules, even Quick Discovery.

</td></tr><tr><td>

Filter

</td><td>

Any process matching the filter will not be added to the Running Processes \[cmdb\_running\_process\] table.

 For example, if you want to filter all svchost.exe processes except the svchost.exe process for IIS classification, the filter definition would be:

 -   name is svchost.exe
-   parameters does not contain iissvcs
 For information on setting filter conditions see: [Condition builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_ConditionBuilder.md)

</td></tr><tr><td>

Case sensitive

</td><td>

Applies to the Filter field. If case sensitive is checked, the filter may pull more or less information than you want. Default is off.

</td></tr><tr><td>

OOB filters

</td><td>

There are Linux and Windows filters to choose from. See [Out-of-the-box process filters](out-of-the-box-process-filters.md) for more details.

</td></tr></tbody>
</table>3.  Enter the details and select **Submit**.


-   **[Out-of-the-box process filters](out-of-the-box-process-filters.md)**  
There are a variety of Linux and Windows out-of-the-box running process filters that are turned on and used for filtering processes.

**Parent Topic:**[Advanced Discovery configuration](c_DiscoveryExtendedCapabilities.md)

