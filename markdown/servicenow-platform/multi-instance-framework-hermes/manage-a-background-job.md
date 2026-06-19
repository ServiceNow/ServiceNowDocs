---
title: Manage a background job in Hermes Messaging Service
description: Manage background jobs in Hermes Messaging Service to control when and how often scheduled tasks run. You can make a job inactive, re-enable it, or adjust its interval from the Hermes Settings page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/multi-instance-framework-hermes/manage-a-background-job.html
release: australia
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: task
last_updated: "2026-05-21"
reading_time_minutes: 1
keywords: [Hermes, Hermes settings, Hermes configuration, background jobs, hermes\_admin, maint, scheduled jobs]
breadcrumb: [Managing Hermes settings, Administer, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Manage a background job in Hermes Messaging Service

Manage background jobs in Hermes Messaging Service to control when and how often scheduled tasks run. You can make a job inactive, re-enable it, or adjust its interval from the Hermes Settings page.

## Before you begin

Role required: maint or hermes\_admin

## About this task

For a list of Hermes background jobs and their default frequencies, see [Hermes background jobs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/multi-instance-framework-hermes/hermes-settings-background-jobs.md).

## Procedure

1.  Navigate to **All** &gt; **Hermes Messaging Service** &gt; **Settings**.

2.  Navigate to the settings category whose background job you plan to manage.

    Each category lists its associated jobs below its properties table.

3.  Select the background job link, such as **Hermes IP ACL Publish Job** or **Hermes Kafka Client Metrics Collection**.

    The Schedule Item record for the job opens in a new window.

4.  In the Schedule Item record for the job, modify the related setting.

<table id="table_jfk_czf_ljc"><thead><tr><th>

Action

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

Change the job state

</td><td>

Select an option from the **State** field:-   **Ready**: The job is active and runs on its next scheduled trigger.
-   **Paused**: The job is inactive and does not run until the state is changed back to **Ready**.


</td></tr><tr><td>

Change the trigger type

</td><td>

Select an option from the **Trigger type** list. The options that are relevant to Hermes Messaging Service background jobs are Interval \(the default\), Daily, or Repeat.

</td></tr><tr><td>

Change the repeat interval for an Interval-type job

</td><td>

Update the **Days**, **Hours**, and **Minutes** fields in the **Repeat** row.For example, the Hermes Active Cluster Heartbeat job runs every 10 minutes by default \(Days: 0, Hours: 00, Minutes: 10\).

</td></tr></tbody>
</table>5.  Select **Update**.


**Parent Topic:**[Managing Hermes settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/multi-instance-framework-hermes/manage-hermes-settings.md)

