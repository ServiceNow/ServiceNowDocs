---
title: Create a batch for Schedule Optimization
description: Create an optimization batch to determine the interval at which optimization should run. Set the start date, batch start time and end time, and run frequency for the related scope.Add scopes to optimization batches or remove a scope from a batch if the number of scopes in a batch becomes too large to manage.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Schedule Optimization, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Create a batch for Schedule Optimization

Create an optimization batch to determine the interval at which optimization should run. Set the start date, batch start time and end time, and run frequency for the related scope.

## Before you begin

Role required: wm\_admin

## About this task

This video demonstrates how to create a batch for Schedule Optimization 

Key considerations for optimizing your schedules:

-   Batch configuration: You can configure up to 36 batches within a 24-hour period for optimizations. Each batch must last at least two hours, and there should be no more than three overlapping batches. For instance, you might have Batch 1 from midnight to 02:00, Batch 2 from 01:00 to 03:00, and Batch 3 from 02:00 to 04:00
-   Frequency settings: Optimizations runs are supported on a continuous or fixed schedule. The default frequency for optimization runs is every seven days. However, you have the flexibility to choose from several options to adjust the run frequency. You can set optimizations to run once, every day, or at intervals of 30, 60, 90, 120, or 180 days, based on your specific needs.
-   Time relative scopes: The start time of a scope is relative to the batch start time. If the batch starts today, but the scope start time is tomorrow, the optimization will focus on agents and tasks for the given scope for the next day.
-   Optimizing across territories: When dealing with agents and tasks spanning multiple territories, the system intelligently consolidates all overlapping territories into a single set. This ensures a streamlined and effective scheduling process.
-   System data: The system tracks task eligibility across territories and calculate associations between territories and their overlaps. This data helps in identifying agent and geographical overlaps, creating a comprehensive list of related territories.

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

At each defined interval, the batch triggers the Schedule Optimization process. Work order tasks are automatically assigned to the most suitable agent, and the **Assigned To** field is updated accordingly. To verify the next scheduled trigger time, see [https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB2142495](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2142495).

**Note:** Schedule Optimization doesn’t detect changes you make to agents or tasks during an optimization run. The system considers changes to agents and tasks during the next optimization run.

You can [View Schedule Optimization logs](view-schedule-optimization-logs.md#) to gather insights from each optimization attempt.

## Add or remove scopes from an optimization batch

Add scopes to optimization batches or remove a scope from a batch if the number of scopes in a batch becomes too large to manage.

### Before you begin

Role required: wm\_admin

### Procedure

1.  Navigate to **All** &gt; **Schedule Optimization** &gt; **Batches**.

2.  Select the optimization batch that you want to add or remove a scope from.

3.  Select **Edit**.

4.  Select the scope.

5.  Either add the scope to or remove the scope from the optimization batch.

    -   To add the scope, select **Add**.
    -   To remove the scope, select **Remove**.
6.  Select **Save**.


