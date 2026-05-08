---
title: Scheduling a workflow
description: In addition to being run based on conditions, workflows can also be scheduled to perform at a particular time, similar to a scheduled job.
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Workflow administration, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Scheduling a workflow

In addition to being run based on conditions, workflows can also be scheduled to perform at a particular time, similar to a scheduled job.

Scheduled workflows do not have a defined current record and do not run on specific records within a table. Due to this behavior, certain activities that depend on a current record, such as **Create Task** or **Catalog Task** are unavailable on scheduled workflows. If your workflow requires one of these activities, consider using a scheduled job that inserts a record to start the workflow instead of using a scheduled workflow.

To schedule a workflow, navigate to **Workflow** &gt; **Scheduled Workflows** and click **New**. Populate the following fields:

<table id="simpletable_imt_4n1_xp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique name for the scheduled workflow.

</td></tr><tr><td>

Workflow

</td><td>

Select an existing published workflow to be triggered at the specified date, time, or interval.

</td></tr><tr><td>

Active

</td><td>

If selected, the scheduled workflow will be triggered at the appropriate time.

</td></tr><tr><td>

Application

</td><td>

Specifies the type of application, such as Global.

</td></tr><tr><td>

Run

</td><td>

A choice list to determine when the workflow should be triggered. Options are:

 -   **Daily:** At a particular hour every day.
-   **Weekly:** On a particular day of the week.
-   **Monthly:** On a particular day of the month
-   **Periodically:** After every set duration.
-   **Once:** At one specific date and time.

</td></tr><tr><td>

Time

</td><td>

For daily/weekly/monthly scheduled workflows, the time of day to run the workflow.

</td></tr><tr><td>

Day

</td><td>

For weekly scheduled workflow, the day of the week to run the workflow. For monthly scheduled workflows, the day of the month to run the workflow.

</td></tr><tr><td>

Repeat Interval

</td><td>

For periodical workflows, the interval between workflows, beginning from the **Starting** date and time.

</td></tr><tr><td>

Starting

</td><td>

For periodical workflows, the first date and time to run the workflow. For scheduled workflows run once, the date and time to run the workflow.

</td></tr></tbody>
</table>**Parent Topic:**[Workflow administration](../../workflow/concept/c_WorkflowAdministration.md)

**Related topics**  


[bundle-platadm.t_CreateAScheduledJob]

