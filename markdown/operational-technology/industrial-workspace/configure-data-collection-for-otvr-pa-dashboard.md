---
title: Configure the data collection for the Operational Technology Vulnerability Response \(PA\) dashboard
description: Configure the data collection for the data shown on the Operational Technology Vulnerability Response \(PA\) dashboard. Scheduled jobs are automated pieces of work that can be performed at a specific time or on a recurring schedule.
locale: en-US
release: zurich
product: Industrial Workspace
classification: industrial-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Setting up the Operational Technology Vulnerability Response \(PA\) dashboard, Configure, Industrial Workspace, Operational Technology]
---

# Configure the data collection for the Operational Technology Vulnerability Response \(PA\) dashboard

Configure the data collection for the data shown on the Operational Technology Vulnerability Response \(PA\) dashboard. Scheduled jobs are automated pieces of work that can be performed at a specific time or on a recurring schedule.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Data Collector** &gt; **Performance Analytics** &gt; **Jobs**.

2.  Apply a filter by selecting the Show/hide filter \(![Show/hide filter icon in the table header.](../../mftg-manufacturing-oper-tech-mgr/image/show-hide-filter-icon.png)\) icon and add the following filters .

    -   `[Application] [is] [Operational Technology Vulnerability Response]`
    -   `[Class] [is] [Scheduled Data Collection]`
    The following scheduled jobs appear when you apply the filter.

    -   \[PA OT VR\] Historical Vulnerability Data Collection

        **Note:** The \[PA OT VR\] Historical Vulnerability Data Collection job is an on-demand job that you only need to execute once. After the historical data is collected, the daily data collection jobs run on a scheduled time every day. For more information about historical data, see [Collect historical data](https://www.servicenow.com/docs/access?context=t_RunHistoricalDataCollection&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

    -   \[PA OT VR\] Daily Collection for Remediation Tasks
    -   \[PA OT VR\] Daily Collection for Vulnerable Items 1
    -   \[PA OT VR\] Daily Collection for Vulnerable Items 2
    -   \[PA OT VR\] Daily Collection for Vulnerable Configuration Items \(CIs\)
3.  To start collecting the data, select a scheduled job record.

4.  Select the check box next to the **Active** field in the Job parameters section and then schedule a time in the **Time** field.

    You can collect the data manually, by using the **Execute Now** button. Otherwise, no data is shown when you view the tab. Only use the **Execute Now** button when you first run the job. The data that is collected after this point should be collected at a scheduled time.

5.  Check if the default schedule collection time works for you.

    The default time is 00:00:00 daily. If you want to change the default collection time, you can change it after activating the job. Make sure that you notify your users about this change.

6.  Repeat steps 3 to 5 for each scheduled job.


## Result

The Operational Technology Vulnerability Response \(PA\) dashboard is now showing the correct data for your users.

## What to do next

Now, you can review the indicator sources and determine if you need to override the default records collection. For more information, see [Review the indicator sources for a larger number of records](update-indicator-source-to-collect-more-records.md).

**Parent Topic:**[Setting up the Operational Technology Vulnerability Response \(PA\) dashboard](../../operational-technology-management/concept/setting-up-the-otvr-pa-dashboard.md)

