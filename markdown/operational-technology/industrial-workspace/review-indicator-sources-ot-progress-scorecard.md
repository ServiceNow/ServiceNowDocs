---
title: Review the indicator sources for a large number of records
description: Review the indicator sources if you need a large number of records. You can override the records collection so that the Operational Technology \(OT\) Progress Scorecard shows more records than the default value of 1 million.
locale: en-US
release: zurich
product: Industrial Workspace
classification: industrial-workspace
topic_type: task
last_updated: "2026-02-24"
reading_time_minutes: 2
breadcrumb: [Setting up the Operational Technology Progress Scorecard, Configure, Industrial Workspace, Operational Technology]
---

# Review the indicator sources for a large number of records

Review the indicator sources if you need a large number of records. You can override the records collection so that the Operational Technology \(OT\) Progress Scorecard shows more records than the default value of 1 million.

## Before you begin

Role required: admin or pa\_admin

## About this task

Due to the migration with Performance Analytics, each indicator of the OT Progress Scorecard can only show 1 million records by default. If you have the admin or pa\_admin role and the records exceed 1 million after running the \[PA OTPSC\] Monthly Data Collection, an error message directs you to the job logs.

**Note:** If you don't have the admin or pa\_admin role and the records exceed 1 million after running the \[PA OTPSC\] Monthly Data Collection job, an error message directs you to contact an administrator for help.

If you have the admin or pa\_admin role, you can check the job logs related list from the link in the error message and filter out the information to see which indicator source has the error. After you find the indicator source with the error, you can change the indicator sources for a larger number of records and override the indicator source data. Then, an error message no longer appears for the other users and the data is shown for the indicator source. For more information about the indicator sources, see [Indicator sources](https://www.servicenow.com/docs/access?context=c_IndicatorSources&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

**Note:** If you need to create new indicators, you must use the site breakdown included in the Industrial Workspace Common. The site breakdown part of the Operational Technology Manager application is deprecated.

The job logs may include errors that aren't about the indicator sources. You must filter the job logs record by the **Level** column and find the error messages about the indicator sources.

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Sources** &gt; **Indicator Sources**.

2.  Apply a filter by selecting the Show/hide filter \(![Show/hide filter icon in the table header.](../../mftg-manufacturing-oper-tech-mgr/image/show-hide-filter-icon.png)\) icon and add the following filter:

    `[Application] [is] [Industrial Workspace Common]`

3.  Select the indicator source record that you need to change.

    You can find which indicator source needs to be adjusted from the job logs link in the error message.

4.  On the **Records Collection** tab, select the check box next to the **Override records collection** field.

5.  In the **Maximum number of fetched records** field, change the value to `XM`.

6.  Select **Update**.


**Parent Topic:**[Setting up the Operational Technology Progress Scorecard](../concept/setting-up-the-ot-progress-scorecard.md)

