---
title: Configure the data collection for the Operational Technology Progress Scorecard
description: Configure the data collection for Operational Technology \(OT\) Progress Scorecard so that you can collect and display the daily data for all indicators from Performance Analytics. This configuration ensures that your OT data is displayed accurately on the scorecard.
locale: en-US
release: australia
product: Industrial Workspace
classification: industrial-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up the Operational Technology Progress Scorecard, Configure, Industrial Workspace, Operational Technology]
---

# Configure the data collection for the Operational Technology Progress Scorecard

Configure the data collection for Operational Technology \(OT\) Progress Scorecard so that you can collect and display the daily data for all indicators from Performance Analytics. This configuration ensures that your OT data is displayed accurately on the scorecard.

## Before you begin

Role required: admin or pa\_admin

## About this task

If you don't run the \[PA OTPSC\] Monthly Data Collection job, then no data is available for the OT Progress Scorecard. If you have the admin role, you see a warning message that prompts you to run the job.

**Note:** If you don't have an admin role, you see a warning message that prompts you to reach out to the administrator for help.

## Procedure

1.  Navigate to **All** &gt; **Data Collector** &gt; **Performance Analytics** &gt; **Jobs**.

    If you're in the OT Progress Scorecard, navigate to the Scheduled Data Collection table by selecting **Run job now** in the error message.

2.  Apply a filter by selecting the Show/hide filter \(![Show/hide filter icon in the table header.](../../mftg-manufacturing-oper-tech-mgr/image/show-hide-filter-icon.png)\) icon and add a filter of `[Name] [is] [[PA OTPSC] Monthly Data Collection]`.

3.  Start collecting the data by selecting the check box next to the **Active** field in the Job parameters section and then schedule a time in the **Time** field.

    You can collect the data manually, by using the **Execute Now** button. Otherwise, no data is shown when you view the tab. Only use the **Execute Now** button when you first run the job. The data that is collected after this point should be collected at a scheduled time.

4.  Check if the default schedule collection time works for you.

    The default time is 00:00:00 at the beginning of every month. If you want to change the default collection time, you can change it after activating the job. Make sure that you notify your users about this change.


## Result

The OT Progress Scorecard is now showing the correct site data for your users.

**Note:** The OT Progress Scorecard uses Performance Analytics. Performance Analytics only saves the scores for 5 months. If want to preserve your scores and compare site data for more than 5 months, see [Activating your Performance Analytics subscription](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/c_PremiumPerformanceAnalytics.md).

**Parent Topic:**[Setting up the Operational Technology Progress Scorecard](../concept/setting-up-the-ot-progress-scorecard.md)

