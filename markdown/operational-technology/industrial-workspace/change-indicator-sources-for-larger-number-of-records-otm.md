---
title: Review the indicator sources for a large number of records
description: Review the indicator sources if you need a large number of records. You can override the records collection so that the Operational Technology \(OT\) Visibility dashboard shows more records than the default value of 1 million.
locale: en-US
release: australia
product: Industrial Workspace
classification: industrial-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setting up the Operational Technology Visibility dashboard, Configure, Industrial Workspace, Operational Technology]
---

# Review the indicator sources for a large number of records

Review the indicator sources if you need a large number of records. You can override the records collection so that the Operational Technology \(OT\) Visibility dashboard shows more records than the default value of 1 million.

## Before you begin

Role required: admin or pa\_admin

## About this task

Due to the migration with Performance Analytics, each indicator of the OT Visibility dashboard can only show 1 million records by default. If you have the admin or pa\_admin role and the records exceed 1 million after running the OT Devices Daily Data Collection job, an error message directs you to the job logs.

**Note:** If you don't have the admin or pa\_admin role and the records exceed 1 million after running the OT Devices Daily Data Collection job, an error message directs you to contact an administrator for help.

If you have the admin or pa\_admin role, you can check the job logs related list from a link in the error message and filter out the information to see which indicator source has the error. After you find the indicator source with the error, you can change the indicator sources for a larger number of records and override the indicator source data. Then, an error message no longer appears for the other users and the data is shown for the indicator source. For more information about the indicator sources, see [Indicator sources](https://www.servicenow.com/docs/access?context=c_IndicatorSources&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

**Note:** If you need to create new indicators, you must use the site breakdown included in the Industrial Workspace Common. The site breakdown part of the Operational Technology Manager application is deprecated.

The job logs may include errors that aren't about the indicator sources. You must filter the job logs record by the **Level** column to find the error messages about the indicator sources.

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Sources** &gt; **Indicator Sources**.

2.  Apply a filter by selecting the Show/hide filter \(![Show/hide filter icon in the table header.](../image/show-hide-filter-icon.png)\) icon and add the following filters.

    -   `[Application] [is] [Operational Technology Manager]`
    -   `[Facts table] [is] [cmdb_ci]`
    After applying the filters, the table shows the following device indicator records:

    -   Benchmark: Inactive OT Devices
    -   Benchmark: Industrial loT
    -   Benchmark: New OT Devices Discovered
    -   Benchmark: OT Computer and Servers
    -   Benchmark: OT Devices
    -   Benchmark: OT Network Gear
    -   Benchmark: Unmapped OT Devices
3.  Select the indicator source record that you need to change.

    You can find which indicator source needs to be adjusted from the job logs link in the error message.

4.  On the **Records Collection** tab, select the check box next to the **Override records collection** field.

5.  In the **Maximum number of fetched records** field, change the value to `XM`.

6.  Select **Update**.


**Parent Topic:**[Setting up the Operational Technology Visibility dashboard](../concept/setting-up-the-ot-devices-dashboard.md)

