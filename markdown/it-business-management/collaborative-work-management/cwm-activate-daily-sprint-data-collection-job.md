---
title: Activate the sprint data job for burnup and burndown widgets
description: Activate the CWM Daily Sprint Data Collection scheduled job to populate data in the predefined burnup and burndown charts in the Team sprint progress dashboard.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/collaborative-work-management/cwm-activate-daily-sprint-data-collection-job.html
release: australia
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: task
last_updated: "2026-08-26"
reading_time_minutes: 1
keywords: [scheduled job, sprint data, burndown chart, burnup chart]
breadcrumb: [Configure, Collaborative Work Management, Strategic Portfolio Management]
---

# Activate the sprint data job for burnup and burndown widgets

Activate the CWM Daily Sprint Data Collection scheduled job to populate data in the predefined burnup and burndown charts in the Team sprint progress dashboard.

## Before you begin

Role required: admin

## About this task

After the job is active, data is collected daily for active sprints. Data appears in the burnup and burndown charts in Board dashboards starting the day after the job begins running.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Filter the **Name** field to locate and open **CWM Daily Sprint Data Collection**.

3.  In the message regarding the application scope, select **Edit this record in Collaborative Work Management**.

4.  Select **System Administrator** in the **Run as** field.

    \[Omitted image "cwm-activate-data-collection-job.png"\] Alt text: Scheduled job form with the Active check box selected.

5.  Select a time zone in the **Run as tz** field.

6.  Select the **Active** check box.

7.  Run the scheduled job by selecting **Execute Now**, or save the record by selecting **Update**.


