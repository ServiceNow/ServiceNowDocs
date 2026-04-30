---
title: Configure the data collection for Operational Technology devices
description: Configure the data collection for Operational Technology \(OT\) devices so that you can collect and display the daily data for all indicators from Performance Analytics. This configuration ensures that your OT data is displayed accurately on the OT Visibility dashboard.
locale: en-US
release: zurich
product: Industrial Workspace
classification: industrial-workspace
topic_type: task
last_updated: "2026-02-24"
reading_time_minutes: 2
breadcrumb: [Setting up the Operational Technology Visibility dashboard, Configure, Industrial Workspace, Operational Technology]
---

# Configure the data collection for Operational Technology devices

Configure the data collection for Operational Technology \(OT\) devices so that you can collect and display the daily data for all indicators from Performance Analytics. This configuration ensures that your OT data is displayed accurately on the OT Visibility dashboard.

## Before you begin

Role required: admin or pa\_admin

## About this task

If the OT Devices Daily Data Collection job hasn't run yet, that means that no data is available for the OT Visibility dashboard and the **Last updated** timestamp is hidden. If you have the admin role, you see the following warning message that prompts you to run the OT Devices Daily Data Collection job:![No data is shown error message on the OT Visibility dashboard that prompts you to run the OT Devices Daily Data Collection Job.](../image/no-data-shown-message.png)

**Note:** If you don't have the pa\_admin role, you see a warning message that prompts you to reach out to the administrator for help.

## Procedure

1.  Navigate to **All** &gt; **Data Collector** &gt; **Performance Analytics** &gt; **Jobs**.

    If you're in the OT Visibility dashboard, you can navigate to the Scheduled Data Collection table by selecting **Run job now** in the error message.

2.  Apply a filter by selecting the Show/hide filter \(![Show/hide filter icon in the table header.](../image/show-hide-filter-icon.png)\) icon and add a filter of `[Name] [is] [OT Devices Daily Data Collection]`.

3.  Start collecting the data by selecting the check box next to the **Active** field in the Job parameters section and then schedule a time in the **Time** field.

    You can collect the data manually by using the **Execute Now** button. Otherwise, no data is shown when you view the dashboard. Only use the **Execute Now** button when you first run the job. The data that is collected after this point should be collected at a scheduled time.

4.  Check if the default schedule collection time works for you.

    The default time is 00:00:00 daily. If you want to change the default collection time, you can change it after activating the job. Make sure that you notify your users about this change.


## Result

The OT Visibility dashboard is now showing the correct data for the collected OT devices for your users.

## What to do next

Now, you can review the indicator sources and determine if you need to override the default records collection. For more information, see [Review the indicator sources for a large number of records](change-indicator-sources-for-larger-number-of-records-otm.md).

**Parent Topic:**[Setting up the Operational Technology Visibility dashboard](../concept/setting-up-the-ot-devices-dashboard.md)

