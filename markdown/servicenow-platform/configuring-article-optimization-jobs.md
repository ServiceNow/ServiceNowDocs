---
title: Configure Article Optimization jobs
description: Article Optimization jobs define a schedule for running scans and their conditional settings. Each job has one or more scans associated with it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/configuring-article-optimization-jobs.html
release: zurich
topic_type: task
last_updated: "2026-07-20"
reading_time_minutes: 1
breadcrumb: [Configuring Knowledge Center, Knowledge Center, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure Article Optimization jobs

Article Optimization jobs define a schedule for running scans and their conditional settings. Each job has one or more scans associated with it.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Knowledge Center** &gt; **Lists** &gt; **Article Optimization** &gt; **Jobs**.

2.  Select **New**.

    1.  To copy and modify an existing job, go to the **sysauto\_kb\_assist\_job** table.

    2.  Open a record and select **Insert and stay** to copy the job.

    3.  Rename the copied job.

3.  Fill out the record form as follows:

    1.  Set the **Query table** field to **Knowledge** \(or another table used to store knowledge articles\).

    2.  Define the filter criteria for the job in the **Query conditions** field.

4.  Define the schedule of the job in the **Run** field and refine it using the **Time Zone** and the **Time** fields \(to stagger job run times and avoid performance issues\).

5.  Select **Save**.

6.  Add or delete scans on the job from the **Related Article Assist Scans** related list.


## Result

The article optimization job is configured.

