---
title: Create a batch for Schedule Optimization
description: Create an optimization batch to determine the interval at which Schedule Optimization should run. Set the start date, batch start time and end time, and run frequency for the related scope.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/field-service-scheduling/create-an-optimization-batch.html
release: brazil
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Batches and scopes, Schedule Optimization, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Create a batch for Schedule Optimization

Create an optimization batch to determine the interval at which Schedule Optimization should run. Set the start date, batch start time and end time, and run frequency for the related scope.

## Before you begin

Verify that your agent work schedules are set up correctly:

-   Work schedule structure: Set up a repeating schedule for each technician, such as a weekly or monthly pattern. Individual day exceptions can override this base schedule. Schedules with single, individual day entries won't work for optimization.
-   Agent availability: Verify technicians are marked as **Free** in their schedules for the time periods covered by the batch. Technicians marked as **Busy** will not receive task assignments.

Role required: wm\_admin

## About this task

\[Omitted video\] Description: This video demonstrates how to create a batch for Schedule Optimization

For information about batch limits, run frequency, and how batches and scopes work together, see [Schedule Optimization batches and scopes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/batches-and-scopes.md).

## Procedure

1.  Navigate to **All** &gt; **Schedule Optimization** &gt; **Batch Optimization** &gt; **Batches**.

2.  Select **New**.

3.  Enter a name in the **Name** field.

4.  Set the start date, batch start time, and end time in the relevant fields.

    **Note:** When you activate a batch with a start date in the past, it creates two scheduled jobs: One to run immediately and another to run in the future. When you activate a batch with a future start date, the batch runs at the specified time. To avoid immediate processing, set the batch start date to a future date when you plan to activate the batch.

5.  Determine how often a batch runs, and select a value for **Run Frequency**.

6.  Select **Save**.

7.  Add scopes to the batch.

    -   To create a scope: Complete steps from 8 through 11.
    -   To reuse an existing scope: In the Optimization Scopes tab, select **Edit** to select an existing scope. When you reuse a scope, the system duplicates the selected scope, including all configuration records, and links the duplicate to the batch.
8.  To optimize tasks by assignment groups or territories, select **New** in the **Optimization Scopes** field.

9.  Enter a name in the **Name** field.

10. Select a scheduling attribute configuration in the **Scheduling attribute** field.

11. Set the **Assignment horizon range** to determine the span of time during which the tasks are assigned to the agents.

12. Select **Activate**.

13. Select **Schedule now** to run the batch immediately without affecting the regular scheduled trigger time.

    The **Schedule now** action runs the batch independently of its regular schedule. Using **Schedule now** doesn't change or delay the next scheduled optimization run.


## Result

At each defined interval, the batch triggers the Schedule Optimization process. Work order tasks are automatically assigned to the most suitable technician, and the **Assigned To** field is updated accordingly. To verify the next scheduled trigger time, see [KB2142495](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2142495).

**Note:** Schedule Optimization doesn’t detect changes you make to agents or tasks during an optimization run. It considers changes to technicians and tasks during the next optimization run.

You can [View Schedule Optimization logs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/view-schedule-optimization-logs.md) to gather insights from each optimization attempt.

**Related topics**  


[Batches and scopes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/batches-and-scopes.md)

[Create a scope for Schedule Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/create-an-optimization-job-soe.md)

[Add or remove scopes from an optimization batch](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/add-remove-scopes-batch.md)

